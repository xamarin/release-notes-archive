---
id: 64BE6567-2F08-4024-A20A-CCC2341E1EEB
title: "OpenTK-1.0.dll"
---

# OpenTK-1.0.dll

## Namespace OpenTK

### Type Changed: OpenTK.DisplayDevice

Obsoleted property:

```
[Obsolete ("Use GetDisplay(DisplayIndex) instead.")]
	public static System.Collections.Generic.IList<DisplayDevice> AvailableDisplays { get; }
```

Added method:

```
public static DisplayDevice GetDisplay (DisplayIndex index);
```

### Type Changed: OpenTK.MathHelper

Added methods:

```
public static double DegreesToRadians (double degrees);
	public static double RadiansToDegrees (double radians);
```

### Type Changed: OpenTK.NativeWindow

Added property:

```
public bool CursorVisible { get; set; }
```

Added events:

```
public event System.EventHandler<Input.KeyboardKeyEventArgs> KeyDown;
	public event System.EventHandler<Input.KeyboardKeyEventArgs> KeyUp;
```

Added method:

```
protected virtual void OnKeyUp (Input.KeyboardKeyEventArgs e);
```

### Type Changed: OpenTK.Quaternion

Added constructor:

```
public Quaternion (ref Matrix3 matrix);
```

Added method:

```
[Obsolete ("Use the overload without the ref float scale")]
	public static void Multiply (ref Quaternion quaternion, ref float scale, out Quaternion result);
```

### Type Changed: OpenTK.Quaterniond

Added method:

```
public static void Multiply (ref Quaterniond quaternion, ref double scale, out Quaterniond result);
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

Added method:

```
public static void Transform (ref Vector3 vec, ref Matrix4 mat, out Vector4 result);
```

### Type Changed: OpenTK.Vector3d

Added constructor:

```
public Vector3d (double value);
```

Added method:

```
public static void Transform (ref Vector3d vec, ref Matrix4d mat, out Vector4d result);
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

Added constructors:

```
public Vector4d (double value);

	[Obsolete ("Use the Vector4d (Vector3d, double) constructor instead")]
	public Vector4d (Vector3 v, double w);
```

### Type Changed: OpenTK.Vector4h

Added constructors:

```
public Vector4h (Half value);
	public Vector4h (float value);
```

### New Type OpenTK.DisplayIndex

```
[Serializable]
public enum DisplayIndex {
	Default = -1,
	Fifth = 4,
	First = 0,
	Fourth = 3,
	Primary = -1,
	Second = 1,
	Sixth = 5,
	Third = 2,
}
```

### New Type OpenTK.Matrix3

```
[Serializable]
public struct Matrix3, System.IEquatable<Matrix3> {
	// constructors
	public Matrix3 (ref Matrix3 matrix);
	public Matrix3 (float r0c0, float r0c1, float r0c2, float r1c0, float r1c1, float r1c2, float r2c0, float r2c1, float r2c2);
	public Matrix3 (float[] floatArray);
	public Matrix3 (Quaterniond quaternion);
	// fields
	public static Matrix3 Identity;
	public float R0C0;
	public float R0C1;
	public float R0C2;
	public float R1C0;
	public float R1C1;
	public float R1C2;
	public float R2C0;
	public float R2C1;
	public float R2C2;
	public static Matrix3 Zero;
	// properties
	public float Determinant { get; }
	public float Item { get; set; }
	public float Item { get; set; }
	// methods
	public static void Add (ref Matrix3 left, ref Matrix3 right, out Matrix3 result);
	public void Add (ref Matrix3 matrix, out Matrix3 result);
	public void Add (ref Matrix3 matrix);
	public static bool Equals (ref Matrix3 left, ref Matrix3 right);
	public virtual bool Equals (Matrix3 matrix);
	public bool Equals (ref Matrix3 matrix);
	public bool EqualsApprox (ref Matrix3 matrix, float tolerance);
	public static bool EqualsApprox (ref Matrix3 left, ref Matrix3 right, float tolerance);
	public override int GetHashCode ();
	public void Multiply (float scalar);
	public void Multiply (ref Matrix3 matrix);
	public void Multiply (float scalar, out Matrix3 result);
	public static void Multiply (ref Matrix3 left, ref Matrix3 right, out Matrix3 result);
	public static void Multiply (ref Matrix3 matrix, float scalar, out Matrix3 result);
	public void Multiply (ref Matrix3 matrix, out Matrix3 result);
	public static System.IntPtr op_Explicit (Matrix3 matrix);
	public static float* op_Explicit (Matrix3 matrix);
	public static float[] op_Explicit (Matrix3 matrix);
	public void Rotate (float angle);
	public void Rotate (float angle, out Matrix3 result);
	public static void Rotate (ref Matrix3 matrix, float angle, out Matrix3 result);
	public static void RotateMatrix (float angle, out Matrix3 result);
	public void Subtract (ref Matrix3 matrix);
	public static void Subtract (ref Matrix3 left, ref Matrix3 right, out Matrix3 result);
	public void Subtract (ref Matrix3 matrix, out Matrix3 result);
	public Quaternion ToQuaternion ();
	public override string ToString ();
	public static void Transform (ref Matrix3 matrix, ref Vector3 vector, out Vector3 result);
	public void Transform (ref Vector3 vector);
	public void Transform (ref Vector3 vector, out Vector3 result);
	public static void Transform (ref Matrix3 matrix, ref Vector3 vector);
	public static void Transpose (ref Matrix3 matrix, out Matrix3 result);
	public void Transpose (out Matrix3 result);
	public void Transpose ();
}
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
protected override void ~GraphicsContext ();
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

## Namespace OpenTK.Graphics.ES10

### Type Changed: OpenTK.Graphics.ES10.All

Added values:

```
Gl3DcXAmd = 34809,
	Gl3DcXyAmd = 34810,
```

### Type Changed: OpenTK.Graphics.ES10.GL

Obsoleted methods:

```
[Obsolete ("Use the method in an extension subclass")]
	public static void ClipPlanefIMG (All p, float* eqn);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ClipPlanefIMG (All p, ref float eqn);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ClipPlanefIMG (All p, float[] eqn);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ClipPlanexIMG (All p, int* eqn);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ClipPlanexIMG (All p, ref int eqn);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ClipPlanexIMG (All p, int[] eqn);

	[Obsolete ("Use the method in an extension subclass")]
	public static void DisableDriverControlQCOM (uint driverControl);

	[Obsolete ("Use the method in an extension subclass")]
	public static void DisableDriverControlQCOM (int driverControl);

	[Obsolete ("Use the method in an extension subclass")]
	public static void EnableDriverControlQCOM (uint driverControl);

	[Obsolete ("Use the method in an extension subclass")]
	public static void EnableDriverControlQCOM (int driverControl);

	[Obsolete ("Use the method in an extension subclass")]
	public static void EndTilingQCOM (int preserveMask);

	[Obsolete ("Use the method in an extension subclass")]
	public static void EndTilingQCOM (uint preserveMask);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM<T1> (All target, out T1 params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM<T1> (All target, T1[0...,0...,0...] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM<T1> (All target, T1[0...,0...] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM<T1> (All target, T1[] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM (All target, System.IntPtr params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (uint* buffers, int maxBuffers, int* numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (ref uint buffers, int maxBuffers, ref int numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (uint[] buffers, int maxBuffers, int[] numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (int* buffers, int maxBuffers, int* numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (ref int buffers, int maxBuffers, ref int numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (int[] buffers, int maxBuffers, int[] numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (uint* framebuffers, int maxFramebuffers, int* numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (ref uint framebuffers, int maxFramebuffers, ref int numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (uint[] framebuffers, int maxFramebuffers, int[] numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (int* framebuffers, int maxFramebuffers, int* numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (ref int framebuffers, int maxFramebuffers, ref int numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (int[] framebuffers, int maxFramebuffers, int[] numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (uint program, All shadertype, string source, int* length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (uint program, All shadertype, string source, ref int length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (uint program, All shadertype, string source, int[] length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (int program, All shadertype, string source, int* length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (int program, All shadertype, string source, ref int length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (int program, All shadertype, string source, int[] length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (uint* programs, int maxPrograms, int* numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (ref uint programs, int maxPrograms, ref int numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (uint[] programs, int maxPrograms, int[] numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (int* programs, int maxPrograms, int* numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (ref int programs, int maxPrograms, ref int numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (int[] programs, int maxPrograms, int[] numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (uint* renderbuffers, int maxRenderbuffers, int* numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (ref uint renderbuffers, int maxRenderbuffers, ref int numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (uint[] renderbuffers, int maxRenderbuffers, int[] numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (int* renderbuffers, int maxRenderbuffers, int* numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (ref int renderbuffers, int maxRenderbuffers, ref int numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (int[] renderbuffers, int maxRenderbuffers, int[] numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (uint* shaders, int maxShaders, int* numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (ref uint shaders, int maxShaders, ref int numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (uint[] shaders, int maxShaders, int[] numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (int* shaders, int maxShaders, int* numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (ref int shaders, int maxShaders, ref int numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (int[] shaders, int maxShaders, int[] numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (uint texture, All face, int level, All pname, int* params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (uint texture, All face, int level, All pname, ref int params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (uint texture, All face, int level, All pname, int[] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (int texture, All face, int level, All pname, int* params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (int texture, All face, int level, All pname, ref int params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (int texture, All face, int level, All pname, int[] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, out T10 texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...,0...] texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...] texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[] texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, System.IntPtr texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (uint* textures, int maxTextures, int* numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (ref uint textures, int maxTextures, ref int numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (uint[] textures, int maxTextures, int[] numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (int* textures, int maxTextures, int* numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (ref int textures, int maxTextures, ref int numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (int[] textures, int maxTextures, int[] numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static bool ExtIsProgramBinaryQCOM (int program);

	[Obsolete ("Use the method in an extension subclass")]
	public static bool ExtIsProgramBinaryQCOM (uint program);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtTexObjectStateOverrideiQCOM (All target, All pname, int param);

	[Obsolete ("Use the method in an extension subclass")]
	public static void FramebufferTexture2DMultisampleIMG (All target, All attachment, All textarget, int texture, int level, int samples);

	[Obsolete ("Use the method in an extension subclass")]
	public static void FramebufferTexture2DMultisampleIMG (All target, All attachment, All textarget, uint texture, int level, int samples);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (int* num, int size, uint* driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (int* num, int size, int* driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (out int num, int size, out uint driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (out int num, int size, out int driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (int[] num, int size, uint[] driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (int[] num, int size, int[] driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (uint driverControl, int bufSize, int* length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (uint driverControl, int bufSize, out int length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (uint driverControl, int bufSize, int[] length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (int driverControl, int bufSize, int* length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (int driverControl, int bufSize, out int length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (int driverControl, int bufSize, int[] length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void RenderbufferStorageMultisampleIMG (All target, int samples, All internalformat, int width, int height);

	[Obsolete ("Use the method in an extension subclass")]
	public static void StartTilingQCOM (uint x, uint y, uint width, uint height, uint preserveMask);

	[Obsolete ("Use the method in an extension subclass")]
	public static void StartTilingQCOM (int x, int y, int width, int height, int preserveMask);
```

### New Type OpenTK.Graphics.ES10.Img

```
public static class Img {
	// methods
	public static void ClipPlane (All p, float[] eqn);
	public static void ClipPlane (All p, ref float eqn);
	public static void ClipPlane (All p, float* eqn);
	public static void ClipPlanex (All p, int* eqn);
	public static void ClipPlanex (All p, ref int eqn);
	public static void ClipPlanex (All p, int[] eqn);
	public static void FramebufferTexture2DMultisample (All target, All attachment, All textarget, int texture, int level, int samples);
	public static void FramebufferTexture2DMultisample (All target, All attachment, All textarget, uint texture, int level, int samples);
	public static void RenderbufferStorageMultisample (All target, int samples, All internalformat, int width, int height);
}
```

### New Type OpenTK.Graphics.ES10.Qcom

```
public static class Qcom {
	// methods
	public static void DisableDriverControl (int driverControl);
	public static void DisableDriverControl (uint driverControl);
	public static void EnableDriverControl (int driverControl);
	public static void EnableDriverControl (uint driverControl);
	public static void EndTiling (uint preserveMask);
	public static void EndTiling (int preserveMask);
	public static void ExtGetBufferPointer<T1> (All target, out T1 params);
	public static void ExtGetBufferPointer<T1> (All target, T1[0...,0...,0...] params);
	public static void ExtGetBufferPointer<T1> (All target, T1[0...,0...] params);
	public static void ExtGetBufferPointer<T1> (All target, T1[] params);
	public static void ExtGetBufferPointer (All target, System.IntPtr params);
	public static void ExtGetBuffers (uint* buffers, int maxBuffers, int* numBuffers);
	public static void ExtGetBuffers (ref uint buffers, int maxBuffers, ref int numBuffers);
	public static void ExtGetBuffers (uint[] buffers, int maxBuffers, int[] numBuffers);
	public static void ExtGetBuffers (int* buffers, int maxBuffers, int* numBuffers);
	public static void ExtGetBuffers (ref int buffers, int maxBuffers, ref int numBuffers);
	public static void ExtGetBuffers (int[] buffers, int maxBuffers, int[] numBuffers);
	public static void ExtGetFramebuffers (uint* framebuffers, int maxFramebuffers, int* numFramebuffers);
	public static void ExtGetFramebuffers (ref uint framebuffers, int maxFramebuffers, ref int numFramebuffers);
	public static void ExtGetFramebuffers (uint[] framebuffers, int maxFramebuffers, int[] numFramebuffers);
	public static void ExtGetFramebuffers (int* framebuffers, int maxFramebuffers, int* numFramebuffers);
	public static void ExtGetFramebuffers (ref int framebuffers, int maxFramebuffers, ref int numFramebuffers);
	public static void ExtGetFramebuffers (int[] framebuffers, int maxFramebuffers, int[] numFramebuffers);
	public static void ExtGetProgram (ref int programs, int maxPrograms, ref int numPrograms);
	public static void ExtGetProgram (int* programs, int maxPrograms, int* numPrograms);
	public static void ExtGetProgram (uint[] programs, int maxPrograms, int[] numPrograms);
	public static void ExtGetProgram (ref uint programs, int maxPrograms, ref int numPrograms);
	public static void ExtGetProgram (uint* programs, int maxPrograms, int* numPrograms);
	public static void ExtGetProgram (int[] programs, int maxPrograms, int[] numPrograms);
	public static void ExtGetProgramBinarySource (int program, All shadertype, string source, int[] length);
	public static void ExtGetProgramBinarySource (int program, All shadertype, string source, ref int length);
	public static void ExtGetProgramBinarySource (int program, All shadertype, string source, int* length);
	public static void ExtGetProgramBinarySource (uint program, All shadertype, string source, int[] length);
	public static void ExtGetProgramBinarySource (uint program, All shadertype, string source, ref int length);
	public static void ExtGetProgramBinarySource (uint program, All shadertype, string source, int* length);
	public static void ExtGetRenderbuffers (uint* renderbuffers, int maxRenderbuffers, int* numRenderbuffers);
	public static void ExtGetRenderbuffers (ref uint renderbuffers, int maxRenderbuffers, ref int numRenderbuffers);
	public static void ExtGetRenderbuffers (uint[] renderbuffers, int maxRenderbuffers, int[] numRenderbuffers);
	public static void ExtGetRenderbuffers (int* renderbuffers, int maxRenderbuffers, int* numRenderbuffers);
	public static void ExtGetRenderbuffers (ref int renderbuffers, int maxRenderbuffers, ref int numRenderbuffers);
	public static void ExtGetRenderbuffers (int[] renderbuffers, int maxRenderbuffers, int[] numRenderbuffers);
	public static void ExtGetShaders (uint* shaders, int maxShaders, int* numShaders);
	public static void ExtGetShaders (ref uint shaders, int maxShaders, ref int numShaders);
	public static void ExtGetShaders (uint[] shaders, int maxShaders, int[] numShaders);
	public static void ExtGetShaders (int* shaders, int maxShaders, int* numShaders);
	public static void ExtGetShaders (ref int shaders, int maxShaders, ref int numShaders);
	public static void ExtGetShaders (int[] shaders, int maxShaders, int[] numShaders);
	public static void ExtGetTexLevelParameter (uint texture, All face, int level, All pname, int* params);
	public static void ExtGetTexLevelParameter (uint texture, All face, int level, All pname, ref int params);
	public static void ExtGetTexLevelParameter (uint texture, All face, int level, All pname, int[] params);
	public static void ExtGetTexLevelParameter (int texture, All face, int level, All pname, int* params);
	public static void ExtGetTexLevelParameter (int texture, All face, int level, All pname, ref int params);
	public static void ExtGetTexLevelParameter (int texture, All face, int level, All pname, int[] params);
	public static void ExtGetTexSubImage<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, out T10 texels);
	public static void ExtGetTexSubImage<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...,0...] texels);
	public static void ExtGetTexSubImage<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...] texels);
	public static void ExtGetTexSubImage<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[] texels);
	public static void ExtGetTexSubImage (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, System.IntPtr texels);
	public static void ExtGetTextures (uint* textures, int maxTextures, int* numTextures);
	public static void ExtGetTextures (ref uint textures, int maxTextures, ref int numTextures);
	public static void ExtGetTextures (uint[] textures, int maxTextures, int[] numTextures);
	public static void ExtGetTextures (int* textures, int maxTextures, int* numTextures);
	public static void ExtGetTextures (ref int textures, int maxTextures, ref int numTextures);
	public static void ExtGetTextures (int[] textures, int maxTextures, int[] numTextures);
	public static bool ExtIsProgramBinary (uint program);
	public static bool ExtIsProgramBinary (int program);
	public static void ExtTexObjectStateOverride (All target, All pname, int param);
	public static void GetDriverControl (int* num, int size, uint* driverControls);
	public static void GetDriverControl (int* num, int size, int* driverControls);
	public static void GetDriverControl (out int num, int size, out uint driverControls);
	public static void GetDriverControl (out int num, int size, out int driverControls);
	public static void GetDriverControl (int[] num, int size, uint[] driverControls);
	public static void GetDriverControl (int[] num, int size, int[] driverControls);
	public static void GetDriverControlString (uint driverControl, int bufSize, int* length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (uint driverControl, int bufSize, out int length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (uint driverControl, int bufSize, int[] length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (int driverControl, int bufSize, int* length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (int driverControl, int bufSize, out int length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (int driverControl, int bufSize, int[] length, System.Text.StringBuilder driverControlString);
	public static void StartTiling (int x, int y, int width, int height, int preserveMask);
	public static void StartTiling (uint x, uint y, uint width, uint height, uint preserveMask);
}
```

### New Type OpenTK.Graphics.ES10.AmdCompressed3Dctexture

```
[Serializable]
public enum AmdCompressed3Dctexture {
	AmdCompressed3DcTexture = 1,
	Gl3DcXAmd = 34809,
	Gl3DcXyAmd = 34810,
}
```

### New Type OpenTK.Graphics.ES10.AmdCompressedAtctexture

```
[Serializable]
public enum AmdCompressedAtctexture {
	AmdCompressedAtcTexture = 1,
	AtcRgbaExplicitAlphaAmd = 35987,
	AtcRgbaInterpolatedAlphaAmd = 34798,
	AtcRgbAmd = 35986,
}
```

### New Type OpenTK.Graphics.ES10.AppleTexture2DlimitedNpot

```
[Serializable]
public enum AppleTexture2DlimitedNpot {
	AppleTexture2DLimitedNpot = 1,
}
```

### New Type OpenTK.Graphics.ES10.BlendequatiOnrgbOesSameAsBlendequatiOnoes

```
[Serializable]
public enum BlendequatiOnrgbOesSameAsBlendequatiOnoes {
	BlendEquationAlphaOes = 34877,
	BlendEquationRgbOes = 32777,
}
```

### New Type OpenTK.Graphics.ES10.ExtBlendMinmax

```
[Serializable]
public enum ExtBlendMinmax {
	ExtBlendMinmax = 1,
	MaxExt = 32776,
	MinExt = 32775,
}
```

### New Type OpenTK.Graphics.ES10.ExtDiscardFramebuffer

```
[Serializable]
public enum ExtDiscardFramebuffer {
	ColorExt = 6144,
	DepthExt = 6145,
	ExtDiscardFramebuffer = 1,
	StencilExt = 6146,
}
```

### New Type OpenTK.Graphics.ES10.ExtMultiDrawArrays

```
[Serializable]
public enum ExtMultiDrawArrays {
	ExtMultiDrawArrays = 1,
}
```

### New Type OpenTK.Graphics.ES10.ExtReadFormatBgra

```
[Serializable]
public enum ExtReadFormatBgra {
	BgraExt = 32993,
	ExtReadFormatBgra = 1,
	UnsignedShort1555RevExt = 33638,
	UnsignedShort4444RevExt = 33637,
}
```

### New Type OpenTK.Graphics.ES10.ExtTextureFilterAnisotropic

```
[Serializable]
public enum ExtTextureFilterAnisotropic {
	ExtTextureFilterAnisotropic = 1,
	MaxTextureMaxAnisotropyExt = 34047,
	TextureMaxAnisotropyExt = 34046,
}
```

### New Type OpenTK.Graphics.ES10.ExtTextureFormatBgra8888

```
[Serializable]
public enum ExtTextureFormatBgra8888 {
	BgraExt = 32993,
	ExtTextureFormatBgra8888 = 1,
}
```

### New Type OpenTK.Graphics.ES10.ExtTextureLodBias

```
[Serializable]
public enum ExtTextureLodBias {
	ExtTextureLodBias = 1,
	MaxTextureLodBiasExt = 34045,
	TextureFilterControlExt = 34048,
	TextureLodBiasExt = 34049,
}
```

### New Type OpenTK.Graphics.ES10.ImgMultisampledRenderToTexture

```
[Serializable]
public enum ImgMultisampledRenderToTexture {
	FramebufferIncompleteMultisampleImg = 37172,
	ImgMultisampledRenderToTexture = 1,
	MaxSamplesImg = 37173,
	RenderbufferSamplesImg = 37171,
	TextureSamplesImg = 37174,
}
```

### New Type OpenTK.Graphics.ES10.ImgReadFormat

```
[Serializable]
public enum ImgReadFormat {
	BgraImg = 32993,
	ImgReadFormat = 1,
	UnsignedShort4444RevImg = 33637,
}
```

### New Type OpenTK.Graphics.ES10.ImgTextureCompressionPvrtc

```
[Serializable]
public enum ImgTextureCompressionPvrtc {
	CompressedRgbaPvrtc2Bppv1Img = 35843,
	CompressedRgbaPvrtc4Bppv1Img = 35842,
	CompressedRgbPvrtc2Bppv1Img = 35841,
	CompressedRgbPvrtc4Bppv1Img = 35840,
	ImgTextureCompressionPvrtc = 1,
}
```

### New Type OpenTK.Graphics.ES10.ImgTextureEnvEnhancedFixedFunction

```
[Serializable]
public enum ImgTextureEnvEnhancedFixedFunction {
	AddBlendImg = 35849,
	Dot3RgbaImg = 34479,
	FactorAlphaModulateImg = 35847,
	FragmentAlphaModulateImg = 35848,
	ImgTextureEnvEnhancedFixedFunction = 1,
	ModulateColorImg = 35844,
	RecipAddSignedAlphaImg = 35845,
	TextureAlphaModulateImg = 35846,
}
```

### New Type OpenTK.Graphics.ES10.ImgUserClipPlane

```
[Serializable]
public enum ImgUserClipPlane {
	ClipPlane0Img = 12288,
	ClipPlane1Img = 12289,
	ClipPlane2Img = 12290,
	ClipPlane3Img = 12291,
	ClipPlane4Img = 12292,
	ClipPlane5Img = 12293,
	ImgUserClipPlane = 1,
	MaxClipPlanesImg = 3378,
}
```

### New Type OpenTK.Graphics.ES10.NvFence

```
[Serializable]
public enum NvFence {
	AllCompletedNv = 34034,
	FenceConditionNv = 34036,
	FenceStatusNv = 34035,
	NvFence = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesBlendEquationSeparate

```
[Serializable]
public enum OesBlendEquationSeparate {
	OesBlendEquationSeparate = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesBlendFuncSeparate

```
[Serializable]
public enum OesBlendFuncSeparate {
	BlendDstAlphaOes = 32970,
	BlendDstRgbOes = 32968,
	BlendSrcAlphaOes = 32971,
	BlendSrcRgbOes = 32969,
	OesBlendFuncSeparate = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesBlendSubtract

```
[Serializable]
public enum OesBlendSubtract {
	BlendEquationOes = 32777,
	FuncAddOes = 32774,
	FuncReverseSubtractOes = 32779,
	FuncSubtractOes = 32778,
	OesBlendSubtract = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesByteCoordinates

```
[Serializable]
public enum OesByteCoordinates {
	OesByteCoordinates = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesCompressedEtc1Rgb8Texture

```
[Serializable]
public enum OesCompressedEtc1Rgb8Texture {
	Etc1Rgb8Oes = 36196,
	OesCompressedEtc1Rgb8Texture = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesCompressedPalettedTexture

```
[Serializable]
public enum OesCompressedPalettedTexture {
	OesCompressedPalettedTexture = 1,
	Palette4R5G6B5Oes = 35730,
	Palette4Rgb5A1Oes = 35732,
	Palette4Rgb8Oes = 35728,
	Palette4Rgba4Oes = 35731,
	Palette4Rgba8Oes = 35729,
	Palette8R5G6B5Oes = 35735,
	Palette8Rgb5A1Oes = 35737,
	Palette8Rgb8Oes = 35733,
	Palette8Rgba4Oes = 35736,
	Palette8Rgba8Oes = 35734,
}
```

### New Type OpenTK.Graphics.ES10.OesDepth24

```
[Serializable]
public enum OesDepth24 {
	DepthComponent24Oes = 33190,
	OesDepth24 = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesDepth32

```
[Serializable]
public enum OesDepth32 {
	DepthComponent32Oes = 33191,
	OesDepth32 = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesDrawTexture

```
[Serializable]
public enum OesDrawTexture {
	OesDrawTexture = 1,
	TextureCropRectOes = 35741,
}
```

### New Type OpenTK.Graphics.ES10.OesEglImage

```
[Serializable]
public enum OesEglImage {
	OesEglImage = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesEglImageExternal

```
[Serializable]
public enum OesEglImageExternal {
	OesEglImageExternal = 1,
	RequiredTextureImageUnitsOes = 36200,
	SamplerExternalOes = 36198,
	TextureBindingExternalOes = 36199,
	TextureExternalOes = 36197,
}
```

### New Type OpenTK.Graphics.ES10.OesElementIndexUint

```
[Serializable]
public enum OesElementIndexUint {
	OesElementIndexUint = 1,
	UnsignedInt = 5125,
}
```

### New Type OpenTK.Graphics.ES10.OesExtendedMatrixPalette

```
[Serializable]
public enum OesExtendedMatrixPalette {
	OesExtendedMatrixPalette = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesFboRenderMipmap

```
[Serializable]
public enum OesFboRenderMipmap {
	OesFboRenderMipmap = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesFixedPoint

```
[Serializable]
public enum OesFixedPoint {
	FixedOes = 5132,
	OesFixedPoint = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesFramebufferObject

```
[Serializable]
public enum OesFramebufferObject {
	ColorAttachment0Oes = 36064,
	DepthAttachmentOes = 36096,
	DepthComponent16Oes = 33189,
	FramebufferAttachmentObjectNameOes = 36049,
	FramebufferAttachmentObjectTypeOes = 36048,
	FramebufferAttachmentTextureCubeMapFaceOes = 36051,
	FramebufferAttachmentTextureLevelOes = 36050,
	FramebufferBindingOes = 36006,
	FramebufferCompleteOes = 36053,
	FramebufferIncompleteAttachmentOes = 36054,
	FramebufferIncompleteDimensionsOes = 36057,
	FramebufferIncompleteFormatsOes = 36058,
	FramebufferIncompleteMissingAttachmentOes = 36055,
	FramebufferOes = 36160,
	FramebufferUnsupportedOes = 36061,
	InvalidFramebufferOperationOes = 1286,
	MaxRenderbufferSizeOes = 34024,
	NoneOes = 0,
	OesFramebufferObject = 1,
	RenderbufferAlphaSizeOes = 36179,
	RenderbufferBindingOes = 36007,
	RenderbufferBlueSizeOes = 36178,
	RenderbufferDepthSizeOes = 36180,
	RenderbufferGreenSizeOes = 36177,
	RenderbufferHeightOes = 36163,
	RenderbufferInternalFormatOes = 36164,
	RenderbufferOes = 36161,
	RenderbufferRedSizeOes = 36176,
	RenderbufferStencilSizeOes = 36181,
	RenderbufferWidthOes = 36162,
	Rgb565Oes = 36194,
	Rgb5A1Oes = 32855,
	Rgba4Oes = 32854,
	StencilAttachmentOes = 36128,
}
```

### New Type OpenTK.Graphics.ES10.OesMapbuffer

```
[Serializable]
public enum OesMapbuffer {
	BufferAccessOes = 35003,
	BufferMappedOes = 35004,
	BufferMapPointerOes = 35005,
	OesMapbuffer = 1,
	WriteOnlyOes = 35001,
}
```

### New Type OpenTK.Graphics.ES10.OesMatrixGet

```
[Serializable]
public enum OesMatrixGet {
	ModelviewMatrixFloatAsIntBitsOes = 35213,
	OesMatrixGet = 1,
	ProjectionMatrixFloatAsIntBitsOes = 35214,
	TextureMatrixFloatAsIntBitsOes = 35215,
}
```

### New Type OpenTK.Graphics.ES10.OesMatrixPalette

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
	OesMatrixPalette = 1,
	WeightArrayBufferBindingOes = 34974,
	WeightArrayOes = 34477,
	WeightArrayPointerOes = 34476,
	WeightArraySizeOes = 34475,
	WeightArrayStrideOes = 34474,
	WeightArrayTypeOes = 34473,
}
```

### New Type OpenTK.Graphics.ES10.OesPackedDepthStencil

```
[Serializable]
public enum OesPackedDepthStencil {
	Depth24Stencil8Oes = 35056,
	DepthStencilOes = 34041,
	OesPackedDepthStencil = 1,
	UnsignedInt248Oes = 34042,
}
```

### New Type OpenTK.Graphics.ES10.OesPointSizeArray

```
[Serializable]
public enum OesPointSizeArray {
	OesPointSizeArray = 1,
	PointSizeArrayBufferBindingOes = 35743,
	PointSizeArrayOes = 35740,
	PointSizeArrayPointerOes = 35212,
	PointSizeArrayStrideOes = 35211,
	PointSizeArrayTypeOes = 35210,
}
```

### New Type OpenTK.Graphics.ES10.OesPointSprite

```
[Serializable]
public enum OesPointSprite {
	CoordReplaceOes = 34914,
	OesPointSprite = 1,
	PointSpriteOes = 34913,
}
```

### New Type OpenTK.Graphics.ES10.OesQueryMatrix

```
[Serializable]
public enum OesQueryMatrix {
	OesQueryMatrix = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesReadFormat

```
[Serializable]
public enum OesReadFormat {
	ImplementationColorReadFormatOes = 35739,
	ImplementationColorReadTypeOes = 35738,
	OesReadFormat = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesRgb8Rgba8

```
[Serializable]
public enum OesRgb8Rgba8 {
	OesRgb8Rgba8 = 1,
	Rgb8Oes = 32849,
	Rgba8Oes = 32856,
}
```

### New Type OpenTK.Graphics.ES10.OesSinglePrecision

```
[Serializable]
public enum OesSinglePrecision {
	OesSinglePrecision = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesStencil1

```
[Serializable]
public enum OesStencil1 {
	OesStencil1 = 1,
	StencilIndex1Oes = 36166,
}
```

### New Type OpenTK.Graphics.ES10.OesStencil4

```
[Serializable]
public enum OesStencil4 {
	OesStencil4 = 1,
	StencilIndex4Oes = 36167,
}
```

### New Type OpenTK.Graphics.ES10.OesStencil8

```
[Serializable]
public enum OesStencil8 {
	OesStencil8 = 1,
	StencilIndex8Oes = 36168,
}
```

### New Type OpenTK.Graphics.ES10.OesStencilWrap

```
[Serializable]
public enum OesStencilWrap {
	DecrWrapOes = 34056,
	IncrWrapOes = 34055,
	OesStencilWrap = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesTextureCubeMap

```
[Serializable]
public enum OesTextureCubeMap {
	MaxCubeMapTextureSizeOes = 34076,
	NormalMapOes = 34065,
	OesTextureCubeMap = 1,
	ReflectionMapOes = 34066,
	TextureBindingCubeMapOes = 34068,
	TextureCubeMapNegativeXOes = 34070,
	TextureCubeMapNegativeYOes = 34072,
	TextureCubeMapNegativeZOes = 34074,
	TextureCubeMapOes = 34067,
	TextureCubeMapPositiveXOes = 34069,
	TextureCubeMapPositiveYOes = 34071,
	TextureCubeMapPositiveZOes = 34073,
	TextureGenModeOes = 9472,
	TextureGenStrOes = 36192,
}
```

### New Type OpenTK.Graphics.ES10.OesTextureEnvCrossbar

```
[Serializable]
public enum OesTextureEnvCrossbar {
	OesTextureEnvCrossbar = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesTextureMirroredRepeat

```
[Serializable]
public enum OesTextureMirroredRepeat {
	MirroredRepeatOes = 33648,
	OesTextureMirroredRepeat = 1,
}
```

### New Type OpenTK.Graphics.ES10.OesVertexArrayObject

```
[Serializable]
public enum OesVertexArrayObject {
	OesVertexArrayObject = 1,
	VertexArrayBindingOes = 34229,
}
```

### New Type OpenTK.Graphics.ES10.OpenGlEsCoreVersions

```
[Serializable]
public enum OpenGlEsCoreVersions {
	VersionEsCl10 = 1,
	VersionEsCl11 = 1,
	VersionEsCm10 = 1,
	VersionEsCm11 = 1,
}
```

### New Type OpenTK.Graphics.ES10.QcomDriverControl

```
[Serializable]
public enum QcomDriverControl {
	QcomDriverControl = 1,
}
```

### New Type OpenTK.Graphics.ES10.QcomExtendedGet

```
[Serializable]
public enum QcomExtendedGet {
	QcomExtendedGet = 1,
	StateRestore = 35804,
	TextureDepthQcom = 35796,
	TextureFormatQcom = 35798,
	TextureHeightQcom = 35795,
	TextureImageValidQcom = 35800,
	TextureInternalFormatQcom = 35797,
	TextureNumLevelsQcom = 35801,
	TextureObjectValidQcom = 35803,
	TextureTargetQcom = 35802,
	TextureTypeQcom = 35799,
	TextureWidthQcom = 35794,
}
```

### New Type OpenTK.Graphics.ES10.QcomExtendedGet2

```
[Serializable]
public enum QcomExtendedGet2 {
	QcomExtendedGet2 = 1,
}
```

### New Type OpenTK.Graphics.ES10.QcomPerfmonGlobalMode

```
[Serializable]
public enum QcomPerfmonGlobalMode {
	PerfmonGlobalModeQcom = 36768,
	QcomPerfmonGlobalMode = 1,
}
```

### New Type OpenTK.Graphics.ES10.QcomTiledRendering

```
[Serializable]
public enum QcomTiledRendering {
	ColorBufferBit0Qcom = 1,
	ColorBufferBit1Qcom = 2,
	ColorBufferBit2Qcom = 4,
	ColorBufferBit3Qcom = 8,
	ColorBufferBit4Qcom = 16,
	ColorBufferBit5Qcom = 32,
	ColorBufferBit6Qcom = 64,
	ColorBufferBit7Qcom = 128,
	DepthBufferBit0Qcom = 256,
	DepthBufferBit1Qcom = 512,
	DepthBufferBit2Qcom = 1024,
	DepthBufferBit3Qcom = 2048,
	DepthBufferBit4Qcom = 4096,
	DepthBufferBit5Qcom = 8192,
	DepthBufferBit6Qcom = 16384,
	DepthBufferBit7Qcom = 32768,
	MultisampleBufferBit0Qcom = 16777216,
	MultisampleBufferBit1Qcom = 33554432,
	MultisampleBufferBit2Qcom = 67108864,
	MultisampleBufferBit3Qcom = 134217728,
	MultisampleBufferBit4Qcom = 268435456,
	MultisampleBufferBit5Qcom = 536870912,
	MultisampleBufferBit6Qcom = 1073741824,
	MultisampleBufferBit7Qcom = -2147483648,
	QcomTiledRendering = 1,
	StencilBufferBit0Qcom = 65536,
	StencilBufferBit1Qcom = 131072,
	StencilBufferBit2Qcom = 262144,
	StencilBufferBit3Qcom = 524288,
	StencilBufferBit4Qcom = 1048576,
	StencilBufferBit5Qcom = 2097152,
	StencilBufferBit6Qcom = 4194304,
	StencilBufferBit7Qcom = 8388608,
}
```

### New Type OpenTK.Graphics.ES10.QcomWriteonlyRendering

```
[Serializable]
public enum QcomWriteonlyRendering {
	QcomWriteonlyRendering = 1,
	WriteonlyRenderingQcom = 34851,
}
```

## Namespace OpenTK.Graphics.ES11

### Type Changed: OpenTK.Graphics.ES11.All

Added values:

```
Gl3DcXAmd = 34809,
	Gl3DcXyAmd = 34810,
```

### Type Changed: OpenTK.Graphics.ES11.GL

Obsoleted methods:

```
[Obsolete ("Use the method in an extension subclass")]
	public static void ClipPlanefIMG (All p, float* eqn);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ClipPlanefIMG (All p, ref float eqn);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ClipPlanefIMG (All p, float[] eqn);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ClipPlanexIMG (All p, int* eqn);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ClipPlanexIMG (All p, ref int eqn);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ClipPlanexIMG (All p, int[] eqn);

	[Obsolete ("Use the method in an extension subclass")]
	public static void DisableDriverControlQCOM (uint driverControl);

	[Obsolete ("Use the method in an extension subclass")]
	public static void DisableDriverControlQCOM (int driverControl);

	[Obsolete ("Use the method in an extension subclass")]
	public static void EnableDriverControlQCOM (uint driverControl);

	[Obsolete ("Use the method in an extension subclass")]
	public static void EnableDriverControlQCOM (int driverControl);

	[Obsolete ("Use the method in an extension subclass")]
	public static void EndTilingQCOM (int preserveMask);

	[Obsolete ("Use the method in an extension subclass")]
	public static void EndTilingQCOM (uint preserveMask);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM<T1> (All target, out T1 params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM<T1> (All target, T1[0...,0...,0...] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM<T1> (All target, T1[0...,0...] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM<T1> (All target, T1[] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM (All target, System.IntPtr params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (uint* buffers, int maxBuffers, int* numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (ref uint buffers, int maxBuffers, ref int numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (uint[] buffers, int maxBuffers, int[] numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (int* buffers, int maxBuffers, int* numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (ref int buffers, int maxBuffers, ref int numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (int[] buffers, int maxBuffers, int[] numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (uint* framebuffers, int maxFramebuffers, int* numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (ref uint framebuffers, int maxFramebuffers, ref int numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (uint[] framebuffers, int maxFramebuffers, int[] numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (int* framebuffers, int maxFramebuffers, int* numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (ref int framebuffers, int maxFramebuffers, ref int numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (int[] framebuffers, int maxFramebuffers, int[] numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (uint program, All shadertype, string source, int* length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (uint program, All shadertype, string source, ref int length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (uint program, All shadertype, string source, int[] length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (int program, All shadertype, string source, int* length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (int program, All shadertype, string source, ref int length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (int program, All shadertype, string source, int[] length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (uint* programs, int maxPrograms, int* numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (ref uint programs, int maxPrograms, ref int numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (uint[] programs, int maxPrograms, int[] numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (int* programs, int maxPrograms, int* numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (ref int programs, int maxPrograms, ref int numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (int[] programs, int maxPrograms, int[] numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (uint* renderbuffers, int maxRenderbuffers, int* numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (ref uint renderbuffers, int maxRenderbuffers, ref int numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (uint[] renderbuffers, int maxRenderbuffers, int[] numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (int* renderbuffers, int maxRenderbuffers, int* numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (ref int renderbuffers, int maxRenderbuffers, ref int numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (int[] renderbuffers, int maxRenderbuffers, int[] numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (uint* shaders, int maxShaders, int* numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (ref uint shaders, int maxShaders, ref int numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (uint[] shaders, int maxShaders, int[] numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (int* shaders, int maxShaders, int* numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (ref int shaders, int maxShaders, ref int numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (int[] shaders, int maxShaders, int[] numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (uint texture, All face, int level, All pname, int* params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (uint texture, All face, int level, All pname, ref int params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (uint texture, All face, int level, All pname, int[] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (int texture, All face, int level, All pname, int* params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (int texture, All face, int level, All pname, ref int params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (int texture, All face, int level, All pname, int[] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, out T10 texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...,0...] texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...] texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[] texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, System.IntPtr texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (uint* textures, int maxTextures, int* numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (ref uint textures, int maxTextures, ref int numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (uint[] textures, int maxTextures, int[] numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (int* textures, int maxTextures, int* numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (ref int textures, int maxTextures, ref int numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (int[] textures, int maxTextures, int[] numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static bool ExtIsProgramBinaryQCOM (int program);

	[Obsolete ("Use the method in an extension subclass")]
	public static bool ExtIsProgramBinaryQCOM (uint program);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtTexObjectStateOverrideiQCOM (All target, All pname, int param);

	[Obsolete ("Use the method in an extension subclass")]
	public static void FramebufferTexture2DMultisampleIMG (All target, All attachment, All textarget, int texture, int level, int samples);

	[Obsolete ("Use the method in an extension subclass")]
	public static void FramebufferTexture2DMultisampleIMG (All target, All attachment, All textarget, uint texture, int level, int samples);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (int* num, int size, uint* driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (int* num, int size, int* driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (out int num, int size, out uint driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (out int num, int size, out int driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (int[] num, int size, uint[] driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (int[] num, int size, int[] driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (uint driverControl, int bufSize, int* length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (uint driverControl, int bufSize, out int length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (uint driverControl, int bufSize, int[] length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (int driverControl, int bufSize, int* length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (int driverControl, int bufSize, out int length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (int driverControl, int bufSize, int[] length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void RenderbufferStorageMultisampleIMG (All target, int samples, All internalformat, int width, int height);

	[Obsolete ("Use the method in an extension subclass")]
	public static void StartTilingQCOM (uint x, uint y, uint width, uint height, uint preserveMask);

	[Obsolete ("Use the method in an extension subclass")]
	public static void StartTilingQCOM (int x, int y, int width, int height, int preserveMask);
```

### New Type OpenTK.Graphics.ES11.Img

```
public static class Img {
	// methods
	public static void ClipPlane (All p, float[] eqn);
	public static void ClipPlane (All p, ref float eqn);
	public static void ClipPlane (All p, float* eqn);
	public static void ClipPlanex (All p, int* eqn);
	public static void ClipPlanex (All p, ref int eqn);
	public static void ClipPlanex (All p, int[] eqn);
	public static void FramebufferTexture2DMultisample (All target, All attachment, All textarget, int texture, int level, int samples);
	public static void FramebufferTexture2DMultisample (All target, All attachment, All textarget, uint texture, int level, int samples);
	public static void RenderbufferStorageMultisample (All target, int samples, All internalformat, int width, int height);
}
```

### New Type OpenTK.Graphics.ES11.Qcom

```
public static class Qcom {
	// methods
	public static void DisableDriverControl (int driverControl);
	public static void DisableDriverControl (uint driverControl);
	public static void EnableDriverControl (int driverControl);
	public static void EnableDriverControl (uint driverControl);
	public static void EndTiling (uint preserveMask);
	public static void EndTiling (int preserveMask);
	public static void ExtGetBufferPointer<T1> (All target, out T1 params);
	public static void ExtGetBufferPointer<T1> (All target, T1[0...,0...,0...] params);
	public static void ExtGetBufferPointer<T1> (All target, T1[0...,0...] params);
	public static void ExtGetBufferPointer<T1> (All target, T1[] params);
	public static void ExtGetBufferPointer (All target, System.IntPtr params);
	public static void ExtGetBuffers (uint* buffers, int maxBuffers, int* numBuffers);
	public static void ExtGetBuffers (ref uint buffers, int maxBuffers, ref int numBuffers);
	public static void ExtGetBuffers (uint[] buffers, int maxBuffers, int[] numBuffers);
	public static void ExtGetBuffers (int* buffers, int maxBuffers, int* numBuffers);
	public static void ExtGetBuffers (ref int buffers, int maxBuffers, ref int numBuffers);
	public static void ExtGetBuffers (int[] buffers, int maxBuffers, int[] numBuffers);
	public static void ExtGetFramebuffers (uint* framebuffers, int maxFramebuffers, int* numFramebuffers);
	public static void ExtGetFramebuffers (ref uint framebuffers, int maxFramebuffers, ref int numFramebuffers);
	public static void ExtGetFramebuffers (uint[] framebuffers, int maxFramebuffers, int[] numFramebuffers);
	public static void ExtGetFramebuffers (int* framebuffers, int maxFramebuffers, int* numFramebuffers);
	public static void ExtGetFramebuffers (ref int framebuffers, int maxFramebuffers, ref int numFramebuffers);
	public static void ExtGetFramebuffers (int[] framebuffers, int maxFramebuffers, int[] numFramebuffers);
	public static void ExtGetProgram (ref int programs, int maxPrograms, ref int numPrograms);
	public static void ExtGetProgram (int* programs, int maxPrograms, int* numPrograms);
	public static void ExtGetProgram (uint[] programs, int maxPrograms, int[] numPrograms);
	public static void ExtGetProgram (ref uint programs, int maxPrograms, ref int numPrograms);
	public static void ExtGetProgram (uint* programs, int maxPrograms, int* numPrograms);
	public static void ExtGetProgram (int[] programs, int maxPrograms, int[] numPrograms);
	public static void ExtGetProgramBinarySource (int program, All shadertype, string source, int[] length);
	public static void ExtGetProgramBinarySource (int program, All shadertype, string source, ref int length);
	public static void ExtGetProgramBinarySource (int program, All shadertype, string source, int* length);
	public static void ExtGetProgramBinarySource (uint program, All shadertype, string source, int[] length);
	public static void ExtGetProgramBinarySource (uint program, All shadertype, string source, ref int length);
	public static void ExtGetProgramBinarySource (uint program, All shadertype, string source, int* length);
	public static void ExtGetRenderbuffers (uint* renderbuffers, int maxRenderbuffers, int* numRenderbuffers);
	public static void ExtGetRenderbuffers (ref uint renderbuffers, int maxRenderbuffers, ref int numRenderbuffers);
	public static void ExtGetRenderbuffers (uint[] renderbuffers, int maxRenderbuffers, int[] numRenderbuffers);
	public static void ExtGetRenderbuffers (int* renderbuffers, int maxRenderbuffers, int* numRenderbuffers);
	public static void ExtGetRenderbuffers (ref int renderbuffers, int maxRenderbuffers, ref int numRenderbuffers);
	public static void ExtGetRenderbuffers (int[] renderbuffers, int maxRenderbuffers, int[] numRenderbuffers);
	public static void ExtGetShaders (uint* shaders, int maxShaders, int* numShaders);
	public static void ExtGetShaders (ref uint shaders, int maxShaders, ref int numShaders);
	public static void ExtGetShaders (uint[] shaders, int maxShaders, int[] numShaders);
	public static void ExtGetShaders (int* shaders, int maxShaders, int* numShaders);
	public static void ExtGetShaders (ref int shaders, int maxShaders, ref int numShaders);
	public static void ExtGetShaders (int[] shaders, int maxShaders, int[] numShaders);
	public static void ExtGetTexLevelParameter (uint texture, All face, int level, All pname, int* params);
	public static void ExtGetTexLevelParameter (uint texture, All face, int level, All pname, ref int params);
	public static void ExtGetTexLevelParameter (uint texture, All face, int level, All pname, int[] params);
	public static void ExtGetTexLevelParameter (int texture, All face, int level, All pname, int* params);
	public static void ExtGetTexLevelParameter (int texture, All face, int level, All pname, ref int params);
	public static void ExtGetTexLevelParameter (int texture, All face, int level, All pname, int[] params);
	public static void ExtGetTexSubImage<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, out T10 texels);
	public static void ExtGetTexSubImage<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...,0...] texels);
	public static void ExtGetTexSubImage<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...] texels);
	public static void ExtGetTexSubImage<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[] texels);
	public static void ExtGetTexSubImage (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, System.IntPtr texels);
	public static void ExtGetTextures (uint* textures, int maxTextures, int* numTextures);
	public static void ExtGetTextures (ref uint textures, int maxTextures, ref int numTextures);
	public static void ExtGetTextures (uint[] textures, int maxTextures, int[] numTextures);
	public static void ExtGetTextures (int* textures, int maxTextures, int* numTextures);
	public static void ExtGetTextures (ref int textures, int maxTextures, ref int numTextures);
	public static void ExtGetTextures (int[] textures, int maxTextures, int[] numTextures);
	public static bool ExtIsProgramBinary (uint program);
	public static bool ExtIsProgramBinary (int program);
	public static void ExtTexObjectStateOverride (All target, All pname, int param);
	public static void GetDriverControl (int* num, int size, uint* driverControls);
	public static void GetDriverControl (int* num, int size, int* driverControls);
	public static void GetDriverControl (out int num, int size, out uint driverControls);
	public static void GetDriverControl (out int num, int size, out int driverControls);
	public static void GetDriverControl (int[] num, int size, uint[] driverControls);
	public static void GetDriverControl (int[] num, int size, int[] driverControls);
	public static void GetDriverControlString (uint driverControl, int bufSize, int* length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (uint driverControl, int bufSize, out int length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (uint driverControl, int bufSize, int[] length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (int driverControl, int bufSize, int* length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (int driverControl, int bufSize, out int length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (int driverControl, int bufSize, int[] length, System.Text.StringBuilder driverControlString);
	public static void StartTiling (int x, int y, int width, int height, int preserveMask);
	public static void StartTiling (uint x, uint y, uint width, uint height, uint preserveMask);
}
```

### New Type OpenTK.Graphics.ES11.AmdCompressed3Dctexture

```
[Serializable]
public enum AmdCompressed3Dctexture {
	AmdCompressed3DcTexture = 1,
	Gl3DcXAmd = 34809,
	Gl3DcXyAmd = 34810,
}
```

### New Type OpenTK.Graphics.ES11.AmdCompressedAtctexture

```
[Serializable]
public enum AmdCompressedAtctexture {
	AmdCompressedAtcTexture = 1,
	AtcRgbaExplicitAlphaAmd = 35987,
	AtcRgbaInterpolatedAlphaAmd = 34798,
	AtcRgbAmd = 35986,
}
```

### New Type OpenTK.Graphics.ES11.AppleTexture2DlimitedNpot

```
[Serializable]
public enum AppleTexture2DlimitedNpot {
	AppleTexture2DLimitedNpot = 1,
}
```

### New Type OpenTK.Graphics.ES11.BlendequatiOnrgbOesSameAsBlendequatiOnoes

```
[Serializable]
public enum BlendequatiOnrgbOesSameAsBlendequatiOnoes {
	BlendEquationAlphaOes = 34877,
	BlendEquationRgbOes = 32777,
}
```

### New Type OpenTK.Graphics.ES11.ExtBlendMinmax

```
[Serializable]
public enum ExtBlendMinmax {
	ExtBlendMinmax = 1,
	MaxExt = 32776,
	MinExt = 32775,
}
```

### New Type OpenTK.Graphics.ES11.ExtDiscardFramebuffer

```
[Serializable]
public enum ExtDiscardFramebuffer {
	ColorExt = 6144,
	DepthExt = 6145,
	ExtDiscardFramebuffer = 1,
	StencilExt = 6146,
}
```

### New Type OpenTK.Graphics.ES11.ExtMultiDrawArrays

```
[Serializable]
public enum ExtMultiDrawArrays {
	ExtMultiDrawArrays = 1,
}
```

### New Type OpenTK.Graphics.ES11.ExtReadFormatBgra

```
[Serializable]
public enum ExtReadFormatBgra {
	BgraExt = 32993,
	ExtReadFormatBgra = 1,
	UnsignedShort1555RevExt = 33638,
	UnsignedShort4444RevExt = 33637,
}
```

### New Type OpenTK.Graphics.ES11.ExtTextureFilterAnisotropic

```
[Serializable]
public enum ExtTextureFilterAnisotropic {
	ExtTextureFilterAnisotropic = 1,
	MaxTextureMaxAnisotropyExt = 34047,
	TextureMaxAnisotropyExt = 34046,
}
```

### New Type OpenTK.Graphics.ES11.ExtTextureFormatBgra8888

```
[Serializable]
public enum ExtTextureFormatBgra8888 {
	BgraExt = 32993,
	ExtTextureFormatBgra8888 = 1,
}
```

### New Type OpenTK.Graphics.ES11.ExtTextureLodBias

```
[Serializable]
public enum ExtTextureLodBias {
	ExtTextureLodBias = 1,
	MaxTextureLodBiasExt = 34045,
	TextureFilterControlExt = 34048,
	TextureLodBiasExt = 34049,
}
```

### New Type OpenTK.Graphics.ES11.ImgMultisampledRenderToTexture

```
[Serializable]
public enum ImgMultisampledRenderToTexture {
	FramebufferIncompleteMultisampleImg = 37172,
	ImgMultisampledRenderToTexture = 1,
	MaxSamplesImg = 37173,
	RenderbufferSamplesImg = 37171,
	TextureSamplesImg = 37174,
}
```

### New Type OpenTK.Graphics.ES11.ImgReadFormat

```
[Serializable]
public enum ImgReadFormat {
	BgraImg = 32993,
	ImgReadFormat = 1,
	UnsignedShort4444RevImg = 33637,
}
```

### New Type OpenTK.Graphics.ES11.ImgTextureCompressionPvrtc

```
[Serializable]
public enum ImgTextureCompressionPvrtc {
	CompressedRgbaPvrtc2Bppv1Img = 35843,
	CompressedRgbaPvrtc4Bppv1Img = 35842,
	CompressedRgbPvrtc2Bppv1Img = 35841,
	CompressedRgbPvrtc4Bppv1Img = 35840,
	ImgTextureCompressionPvrtc = 1,
}
```

### New Type OpenTK.Graphics.ES11.ImgTextureEnvEnhancedFixedFunction

```
[Serializable]
public enum ImgTextureEnvEnhancedFixedFunction {
	AddBlendImg = 35849,
	Dot3RgbaImg = 34479,
	FactorAlphaModulateImg = 35847,
	FragmentAlphaModulateImg = 35848,
	ImgTextureEnvEnhancedFixedFunction = 1,
	ModulateColorImg = 35844,
	RecipAddSignedAlphaImg = 35845,
	TextureAlphaModulateImg = 35846,
}
```

### New Type OpenTK.Graphics.ES11.ImgUserClipPlane

```
[Serializable]
public enum ImgUserClipPlane {
	ClipPlane0Img = 12288,
	ClipPlane1Img = 12289,
	ClipPlane2Img = 12290,
	ClipPlane3Img = 12291,
	ClipPlane4Img = 12292,
	ClipPlane5Img = 12293,
	ImgUserClipPlane = 1,
	MaxClipPlanesImg = 3378,
}
```

### New Type OpenTK.Graphics.ES11.NvFence

```
[Serializable]
public enum NvFence {
	AllCompletedNv = 34034,
	FenceConditionNv = 34036,
	FenceStatusNv = 34035,
	NvFence = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesBlendEquationSeparate

```
[Serializable]
public enum OesBlendEquationSeparate {
	OesBlendEquationSeparate = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesBlendFuncSeparate

```
[Serializable]
public enum OesBlendFuncSeparate {
	BlendDstAlphaOes = 32970,
	BlendDstRgbOes = 32968,
	BlendSrcAlphaOes = 32971,
	BlendSrcRgbOes = 32969,
	OesBlendFuncSeparate = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesBlendSubtract

```
[Serializable]
public enum OesBlendSubtract {
	BlendEquationOes = 32777,
	FuncAddOes = 32774,
	FuncReverseSubtractOes = 32779,
	FuncSubtractOes = 32778,
	OesBlendSubtract = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesByteCoordinates

```
[Serializable]
public enum OesByteCoordinates {
	OesByteCoordinates = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesCompressedEtc1Rgb8Texture

```
[Serializable]
public enum OesCompressedEtc1Rgb8Texture {
	Etc1Rgb8Oes = 36196,
	OesCompressedEtc1Rgb8Texture = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesCompressedPalettedTexture

```
[Serializable]
public enum OesCompressedPalettedTexture {
	OesCompressedPalettedTexture = 1,
	Palette4R5G6B5Oes = 35730,
	Palette4Rgb5A1Oes = 35732,
	Palette4Rgb8Oes = 35728,
	Palette4Rgba4Oes = 35731,
	Palette4Rgba8Oes = 35729,
	Palette8R5G6B5Oes = 35735,
	Palette8Rgb5A1Oes = 35737,
	Palette8Rgb8Oes = 35733,
	Palette8Rgba4Oes = 35736,
	Palette8Rgba8Oes = 35734,
}
```

### New Type OpenTK.Graphics.ES11.OesDepth24

```
[Serializable]
public enum OesDepth24 {
	DepthComponent24Oes = 33190,
	OesDepth24 = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesDepth32

```
[Serializable]
public enum OesDepth32 {
	DepthComponent32Oes = 33191,
	OesDepth32 = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesDrawTexture

```
[Serializable]
public enum OesDrawTexture {
	OesDrawTexture = 1,
	TextureCropRectOes = 35741,
}
```

### New Type OpenTK.Graphics.ES11.OesEglImage

```
[Serializable]
public enum OesEglImage {
	OesEglImage = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesEglImageExternal

```
[Serializable]
public enum OesEglImageExternal {
	OesEglImageExternal = 1,
	RequiredTextureImageUnitsOes = 36200,
	SamplerExternalOes = 36198,
	TextureBindingExternalOes = 36199,
	TextureExternalOes = 36197,
}
```

### New Type OpenTK.Graphics.ES11.OesElementIndexUint

```
[Serializable]
public enum OesElementIndexUint {
	OesElementIndexUint = 1,
	UnsignedInt = 5125,
}
```

### New Type OpenTK.Graphics.ES11.OesExtendedMatrixPalette

```
[Serializable]
public enum OesExtendedMatrixPalette {
	OesExtendedMatrixPalette = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesFboRenderMipmap

```
[Serializable]
public enum OesFboRenderMipmap {
	OesFboRenderMipmap = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesFixedPoint

```
[Serializable]
public enum OesFixedPoint {
	FixedOes = 5132,
	OesFixedPoint = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesFramebufferObject

```
[Serializable]
public enum OesFramebufferObject {
	ColorAttachment0Oes = 36064,
	DepthAttachmentOes = 36096,
	DepthComponent16Oes = 33189,
	FramebufferAttachmentObjectNameOes = 36049,
	FramebufferAttachmentObjectTypeOes = 36048,
	FramebufferAttachmentTextureCubeMapFaceOes = 36051,
	FramebufferAttachmentTextureLevelOes = 36050,
	FramebufferBindingOes = 36006,
	FramebufferCompleteOes = 36053,
	FramebufferIncompleteAttachmentOes = 36054,
	FramebufferIncompleteDimensionsOes = 36057,
	FramebufferIncompleteFormatsOes = 36058,
	FramebufferIncompleteMissingAttachmentOes = 36055,
	FramebufferOes = 36160,
	FramebufferUnsupportedOes = 36061,
	InvalidFramebufferOperationOes = 1286,
	MaxRenderbufferSizeOes = 34024,
	NoneOes = 0,
	OesFramebufferObject = 1,
	RenderbufferAlphaSizeOes = 36179,
	RenderbufferBindingOes = 36007,
	RenderbufferBlueSizeOes = 36178,
	RenderbufferDepthSizeOes = 36180,
	RenderbufferGreenSizeOes = 36177,
	RenderbufferHeightOes = 36163,
	RenderbufferInternalFormatOes = 36164,
	RenderbufferOes = 36161,
	RenderbufferRedSizeOes = 36176,
	RenderbufferStencilSizeOes = 36181,
	RenderbufferWidthOes = 36162,
	Rgb565Oes = 36194,
	Rgb5A1Oes = 32855,
	Rgba4Oes = 32854,
	StencilAttachmentOes = 36128,
}
```

### New Type OpenTK.Graphics.ES11.OesMapbuffer

```
[Serializable]
public enum OesMapbuffer {
	BufferAccessOes = 35003,
	BufferMappedOes = 35004,
	BufferMapPointerOes = 35005,
	OesMapbuffer = 1,
	WriteOnlyOes = 35001,
}
```

### New Type OpenTK.Graphics.ES11.OesMatrixGet

```
[Serializable]
public enum OesMatrixGet {
	ModelviewMatrixFloatAsIntBitsOes = 35213,
	OesMatrixGet = 1,
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
	OesMatrixPalette = 1,
	WeightArrayBufferBindingOes = 34974,
	WeightArrayOes = 34477,
	WeightArrayPointerOes = 34476,
	WeightArraySizeOes = 34475,
	WeightArrayStrideOes = 34474,
	WeightArrayTypeOes = 34473,
}
```

### New Type OpenTK.Graphics.ES11.OesPackedDepthStencil

```
[Serializable]
public enum OesPackedDepthStencil {
	Depth24Stencil8Oes = 35056,
	DepthStencilOes = 34041,
	OesPackedDepthStencil = 1,
	UnsignedInt248Oes = 34042,
}
```

### New Type OpenTK.Graphics.ES11.OesPointSizeArray

```
[Serializable]
public enum OesPointSizeArray {
	OesPointSizeArray = 1,
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
	OesPointSprite = 1,
	PointSpriteOes = 34913,
}
```

### New Type OpenTK.Graphics.ES11.OesQueryMatrix

```
[Serializable]
public enum OesQueryMatrix {
	OesQueryMatrix = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesReadFormat

```
[Serializable]
public enum OesReadFormat {
	ImplementationColorReadFormatOes = 35739,
	ImplementationColorReadTypeOes = 35738,
	OesReadFormat = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesRgb8Rgba8

```
[Serializable]
public enum OesRgb8Rgba8 {
	OesRgb8Rgba8 = 1,
	Rgb8Oes = 32849,
	Rgba8Oes = 32856,
}
```

### New Type OpenTK.Graphics.ES11.OesSinglePrecision

```
[Serializable]
public enum OesSinglePrecision {
	OesSinglePrecision = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesStencil1

```
[Serializable]
public enum OesStencil1 {
	OesStencil1 = 1,
	StencilIndex1Oes = 36166,
}
```

### New Type OpenTK.Graphics.ES11.OesStencil4

```
[Serializable]
public enum OesStencil4 {
	OesStencil4 = 1,
	StencilIndex4Oes = 36167,
}
```

### New Type OpenTK.Graphics.ES11.OesStencil8

```
[Serializable]
public enum OesStencil8 {
	OesStencil8 = 1,
	StencilIndex8Oes = 36168,
}
```

### New Type OpenTK.Graphics.ES11.OesStencilWrap

```
[Serializable]
public enum OesStencilWrap {
	DecrWrapOes = 34056,
	IncrWrapOes = 34055,
	OesStencilWrap = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesTextureCubeMap

```
[Serializable]
public enum OesTextureCubeMap {
	MaxCubeMapTextureSizeOes = 34076,
	NormalMapOes = 34065,
	OesTextureCubeMap = 1,
	ReflectionMapOes = 34066,
	TextureBindingCubeMapOes = 34068,
	TextureCubeMapNegativeXOes = 34070,
	TextureCubeMapNegativeYOes = 34072,
	TextureCubeMapNegativeZOes = 34074,
	TextureCubeMapOes = 34067,
	TextureCubeMapPositiveXOes = 34069,
	TextureCubeMapPositiveYOes = 34071,
	TextureCubeMapPositiveZOes = 34073,
	TextureGenModeOes = 9472,
	TextureGenStrOes = 36192,
}
```

### New Type OpenTK.Graphics.ES11.OesTextureEnvCrossbar

```
[Serializable]
public enum OesTextureEnvCrossbar {
	OesTextureEnvCrossbar = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesTextureMirroredRepeat

```
[Serializable]
public enum OesTextureMirroredRepeat {
	MirroredRepeatOes = 33648,
	OesTextureMirroredRepeat = 1,
}
```

### New Type OpenTK.Graphics.ES11.OesVertexArrayObject

```
[Serializable]
public enum OesVertexArrayObject {
	OesVertexArrayObject = 1,
	VertexArrayBindingOes = 34229,
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

### New Type OpenTK.Graphics.ES11.QcomDriverControl

```
[Serializable]
public enum QcomDriverControl {
	QcomDriverControl = 1,
}
```

### New Type OpenTK.Graphics.ES11.QcomExtendedGet

```
[Serializable]
public enum QcomExtendedGet {
	QcomExtendedGet = 1,
	StateRestore = 35804,
	TextureDepthQcom = 35796,
	TextureFormatQcom = 35798,
	TextureHeightQcom = 35795,
	TextureImageValidQcom = 35800,
	TextureInternalFormatQcom = 35797,
	TextureNumLevelsQcom = 35801,
	TextureObjectValidQcom = 35803,
	TextureTargetQcom = 35802,
	TextureTypeQcom = 35799,
	TextureWidthQcom = 35794,
}
```

### New Type OpenTK.Graphics.ES11.QcomExtendedGet2

```
[Serializable]
public enum QcomExtendedGet2 {
	QcomExtendedGet2 = 1,
}
```

### New Type OpenTK.Graphics.ES11.QcomPerfmonGlobalMode

```
[Serializable]
public enum QcomPerfmonGlobalMode {
	PerfmonGlobalModeQcom = 36768,
	QcomPerfmonGlobalMode = 1,
}
```

### New Type OpenTK.Graphics.ES11.QcomTiledRendering

```
[Serializable]
public enum QcomTiledRendering {
	ColorBufferBit0Qcom = 1,
	ColorBufferBit1Qcom = 2,
	ColorBufferBit2Qcom = 4,
	ColorBufferBit3Qcom = 8,
	ColorBufferBit4Qcom = 16,
	ColorBufferBit5Qcom = 32,
	ColorBufferBit6Qcom = 64,
	ColorBufferBit7Qcom = 128,
	DepthBufferBit0Qcom = 256,
	DepthBufferBit1Qcom = 512,
	DepthBufferBit2Qcom = 1024,
	DepthBufferBit3Qcom = 2048,
	DepthBufferBit4Qcom = 4096,
	DepthBufferBit5Qcom = 8192,
	DepthBufferBit6Qcom = 16384,
	DepthBufferBit7Qcom = 32768,
	MultisampleBufferBit0Qcom = 16777216,
	MultisampleBufferBit1Qcom = 33554432,
	MultisampleBufferBit2Qcom = 67108864,
	MultisampleBufferBit3Qcom = 134217728,
	MultisampleBufferBit4Qcom = 268435456,
	MultisampleBufferBit5Qcom = 536870912,
	MultisampleBufferBit6Qcom = 1073741824,
	MultisampleBufferBit7Qcom = -2147483648,
	QcomTiledRendering = 1,
	StencilBufferBit0Qcom = 65536,
	StencilBufferBit1Qcom = 131072,
	StencilBufferBit2Qcom = 262144,
	StencilBufferBit3Qcom = 524288,
	StencilBufferBit4Qcom = 1048576,
	StencilBufferBit5Qcom = 2097152,
	StencilBufferBit6Qcom = 4194304,
	StencilBufferBit7Qcom = 8388608,
}
```

### New Type OpenTK.Graphics.ES11.QcomWriteonlyRendering

```
[Serializable]
public enum QcomWriteonlyRendering {
	QcomWriteonlyRendering = 1,
	WriteonlyRenderingQcom = 34851,
}
```

## Namespace OpenTK.Graphics.ES20

### Type Changed: OpenTK.Graphics.ES20.All

Added values:

```
BlendEquationRgb = 32777,
	Gl3DcXAmd = 34809,
	Gl3DcXyAmd = 34810,
	ImgTextureFormatBgra8888 = 1,
```

### Type Changed: OpenTK.Graphics.ES20.BlendingFactorDest

Added values:

```
ConstantAlpha = 32771,
	ConstantColor = 32769,
	DstColor = 774,
	OneMinusConstantAlpha = 32772,
	OneMinusConstantColor = 32770,
	OneMinusDstColor = 775,
	SrcAlphaSaturate = 776,
```

### Type Changed: OpenTK.Graphics.ES20.BlendingFactorSrc

Added values:

```
ConstantAlpha = 32771,
	ConstantColor = 32769,
	DstAlpha = 772,
	One = 1,
	OneMinusConstantAlpha = 32772,
	OneMinusConstantColor = 32770,
	OneMinusDstAlpha = 773,
	OneMinusSrcAlpha = 771,
	OneMinusSrcColor = 769,
	SrcAlpha = 770,
	SrcColor = 768,
	Zero = 0,
```

### Type Changed: OpenTK.Graphics.ES20.DrawElementsType

Added value:

```
UnsignedInt = 5125,
```

### Type Changed: OpenTK.Graphics.ES20.ErrorCode

Added value:

```
InvalidFramebufferOperation = 1286,
```

### Type Changed: OpenTK.Graphics.ES20.GetPName

Added values:

```
ActiveTexture = 34016,
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
	CompressedTextureFormats = 34467,
	CullFace = 2884,
	CurrentProgram = 35725,
	DepthTest = 2929,
	Dither = 3024,
	ElementArrayBufferBinding = 34965,
	FramebufferBinding = 36006,
	GenerateMipmapHint = 33170,
	ImplementationColorReadFormat = 35739,
	ImplementationColorReadType = 35738,
	MaxCombinedTextureImageUnits = 35661,
	MaxCubeMapTextureSize = 34076,
	MaxFragmentUniformVectors = 36349,
	MaxRenderbufferSize = 34024,
	MaxTextureImageUnits = 34930,
	MaxVaryingVectors = 36348,
	MaxVertexAttribs = 34921,
	MaxVertexTextureImageUnits = 35660,
	MaxVertexUniformVectors = 36347,
	NumCompressedTextureFormats = 34466,
	NumShaderBinaryFormats = 36345,
	PolygonOffsetFill = 32823,
	RenderbufferBinding = 36007,
	SampleAlphaToCoverage = 32926,
	SampleCoverage = 32928,
	ScissorTest = 3089,
	ShaderBinaryFormats = 36344,
	ShaderCompiler = 36346,
	StencilTest = 2960,
	Texture2D = 3553,
	TextureBindingCubeMap = 34068,
```

### Type Changed: OpenTK.Graphics.ES20.GetTextureParameter

Added values:

```
TextureMagFilter = 10240,
	TextureMinFilter = 10241,
	TextureWrapS = 10242,
	TextureWrapT = 10243,
```

### Type Changed: OpenTK.Graphics.ES20.GL

Added methods:

```
public static void ActiveTexture (TextureUnit texture);
	public static void BindBuffer (BufferTarget target, uint buffer);
	public static void BindBuffer (BufferTarget target, int buffer);
	public static void BindFramebuffer (FramebufferTarget target, int framebuffer);
	public static void BindFramebuffer (FramebufferTarget target, uint framebuffer);
	public static void BindRenderbuffer (RenderbufferTarget target, int renderbuffer);
	public static void BindRenderbuffer (RenderbufferTarget target, uint renderbuffer);
	public static void BindTexture (TextureTarget target, int texture);
	public static void BindTexture (TextureTarget target, uint texture);
	public static void BlendEquation (BlendEquationMode mode);
	public static void BlendEquationSeparate (BlendEquationMode modeRGB, BlendEquationMode modeAlpha);
	public static void BlendFunc (BlendingFactorSrc sfactor, BlendingFactorDest dfactor);
	public static void BlendFuncSeparate (BlendingFactorSrc srcRGB, BlendingFactorDest dstRGB, BlendingFactorSrc srcAlpha, BlendingFactorDest dstAlpha);
	public static void BufferData (BufferTarget target, System.IntPtr size, System.IntPtr data, BufferUsage usage);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, T2[] data, BufferUsage usage);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, T2[0...,0...] data, BufferUsage usage);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, T2[0...,0...,0...] data, BufferUsage usage);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, out T2 data, BufferUsage usage);
	public static void BufferSubData (BufferTarget target, System.IntPtr offset, System.IntPtr size, System.IntPtr data);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, T3[] data);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, T3[0...,0...] data);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, T3[0...,0...,0...] data);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, out T3 data);
	public static FramebufferErrorCode CheckFramebufferStatus (FramebufferTarget target);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, T7[0...,0...,0...] data);
	public static void CompressedTexImage2D (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, System.IntPtr data);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, T7[] data);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, T7[0...,0...] data);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, out T7 data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, T8[] data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, T8[0...,0...] data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, T8[0...,0...,0...] data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, out T8 data);
	public static void CompressedTexSubImage2D (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, System.IntPtr data);
	public static void CopyTexImage2D (TextureTarget target, int level, PixelInternalFormat internalformat, int x, int y, int width, int height, int border);
	public static void CopyTexSubImage2D (TextureTarget target, int level, int xoffset, int yoffset, int x, int y, int width, int height);
	public static int CreateShader (ShaderType type);
	public static void CullFace (CullFaceMode mode);
	public static void DeleteTexture (uint id);
	public static void DepthFunc (DepthFunction func);
	public static void Disable (EnableCap cap);
	public static void DrawArrays (BeginMode mode, int first, int count);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, out T3 indices);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, T3[0...,0...,0...] indices);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, T3[0...,0...] indices);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, T3[] indices);
	public static void DrawElements (BeginMode mode, int count, DrawElementsType type, System.IntPtr indices);
	public static void Enable (EnableCap cap);
	public static void FramebufferRenderbuffer (FramebufferTarget target, FramebufferSlot attachment, RenderbufferTarget renderbuffertarget, uint renderbuffer);
	public static void FramebufferRenderbuffer (FramebufferTarget target, FramebufferSlot attachment, RenderbufferTarget renderbuffertarget, int renderbuffer);
	public static void FramebufferTexture2D (FramebufferTarget target, FramebufferSlot attachment, TextureTarget textarget, int texture, int level);
	public static void FramebufferTexture2D (FramebufferTarget target, FramebufferSlot attachment, TextureTarget textarget, uint texture, int level);
	public static void FrontFace (FrontFaceDirection mode);
	public static void GenerateMipmap (TextureTarget target);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, int* length, int* size, ActiveAttribType* type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, out int length, out int size, out ActiveAttribType type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, int[] length, int[] size, ActiveAttribType[] type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (int program, int index, int bufsize, int* length, int* size, ActiveAttribType* type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (int program, int index, int bufsize, out int length, out int size, out ActiveAttribType type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (int program, int index, int bufsize, int[] length, int[] size, ActiveAttribType[] type, System.Text.StringBuilder name);
	public static void GetActiveUniform (uint program, uint index, int bufsize, out int length, out int size, out ActiveUniformType type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, int[] length, int[] size, ActiveUniformType[] type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, out int length, out int size, out ActiveUniformType type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, int* length, int* size, ActiveUniformType* type, System.Text.StringBuilder name);
	public static void GetActiveUniform (uint program, uint index, int bufsize, int[] length, int[] size, ActiveUniformType[] type, System.Text.StringBuilder name);
	public static void GetActiveUniform (uint program, uint index, int bufsize, int* length, int* size, ActiveUniformType* type, System.Text.StringBuilder name);
	public static int GetAttribLocation (int program, string name);
	public static int GetAttribLocation (uint program, string name);
	public static void GetBoolean (GetPName pname, bool* params);
	public static void GetBoolean (GetPName pname, out bool params);
	public static void GetBoolean (GetPName pname, bool[] params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, int* params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, out int params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, int[] params);
	public static ErrorCode GetErrorCode ();
	public static void GetFloat (GetPName pname, float* params);
	public static void GetFloat (GetPName pname, out float params);
	public static void GetFloat (GetPName pname, float[] params);
	public static void GetFloat (GetPName pname, out OpenTK.Matrix4 matrix);
	public static void GetFloat (GetPName pname, out OpenTK.Vector4 vector);
	public static void GetFloat (GetPName pname, out OpenTK.Vector3 vector);
	public static void GetFloat (GetPName pname, out OpenTK.Vector2 vector);
	public static void GetFramebufferAttachmentParameter (FramebufferTarget target, FramebufferSlot attachment, FramebufferParameterName pname, int* params);
	public static void GetFramebufferAttachmentParameter (FramebufferTarget target, FramebufferSlot attachment, FramebufferParameterName pname, out int params);
	public static void GetFramebufferAttachmentParameter (FramebufferTarget target, FramebufferSlot attachment, FramebufferParameterName pname, int[] params);
	public static void GetInteger (GetPName pname, int[] params);
	public static void GetInteger (GetPName pname, int* params);
	public static void GetInteger (GetPName pname, out int params);
	public static void GetProgram (uint program, ProgramParameter pname, int* params);
	public static void GetProgram (uint program, ProgramParameter pname, out int params);
	public static void GetProgram (int program, ProgramParameter pname, int* params);
	public static void GetProgram (uint program, ProgramParameter pname, int[] params);
	public static void GetProgram (int program, ProgramParameter pname, out int params);
	public static void GetProgram (int program, ProgramParameter pname, int[] params);
	public static void GetRenderbufferParameter (RenderbufferTarget target, RenderbufferParameterName pname, int[] params);
	public static void GetRenderbufferParameter (RenderbufferTarget target, RenderbufferParameterName pname, out int params);
	public static void GetRenderbufferParameter (RenderbufferTarget target, RenderbufferParameterName pname, int* params);
	public static void GetShader (int shader, ShaderParameter pname, int[] params);
	public static void GetShader (uint shader, ShaderParameter pname, int* params);
	public static void GetShader (uint shader, ShaderParameter pname, int[] params);
	public static void GetShader (int shader, ShaderParameter pname, int* params);
	public static void GetShader (int shader, ShaderParameter pname, out int params);
	public static void GetShader (uint shader, ShaderParameter pname, out int params);
	public static void GetShaderPrecisionFormat (ShaderType shadertype, ShaderPrecision precisiontype, int[] range, int[] precision);
	public static void GetShaderPrecisionFormat (ShaderType shadertype, ShaderPrecision precisiontype, int* range, int* precision);
	public static void GetShaderPrecisionFormat (ShaderType shadertype, ShaderPrecision precisiontype, out int range, out int precision);
	public static string GetString (StringName name);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, int* params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, out int params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, int[] params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, float* params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, out float params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, float[] params);
	public static int GetUniformLocation (int program, string name);
	public static int GetUniformLocation (uint program, string name);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, int* params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, out int params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, int[] params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, float* params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, out float params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, float[] params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, float[] params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, out float params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, float* params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, int[] params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, out int params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, int* params);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, out T2 pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, T2[0...,0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, out T2 pointer);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, T2[0...,0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, T2[0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, T2[] pointer);
	public static void GetVertexAttribPointer (int index, VertexAttribPointerParameter pname, System.IntPtr pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, T2[0...,0...] pointer);
	public static void GetVertexAttribPointer (uint index, VertexAttribPointerParameter pname, System.IntPtr pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, T2[] pointer);
	public static void Hint (HintTarget target, HintMode mode);
	public static bool IsEnabled (EnableCap cap);
	public static void PixelStore (PixelStoreParameter pname, int param);
	public static void ReadPixels (int x, int y, int width, int height, PixelFormat format, PixelType type, System.IntPtr pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, T6[0...,0...] pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, T6[0...,0...,0...] pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, out T6 pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, T6[] pixels);
	public static void RenderbufferStorage (RenderbufferTarget target, RenderbufferInternalFormat internalformat, int width, int height);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary (int n, ref uint shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary (int n, uint* shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary (int n, uint[] shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary (int n, ref int shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary (int n, int[] shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary (int n, int* shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void StencilFunc (StencilFunction func, int ref, uint mask);
	public static void StencilFunc (StencilFunction func, int ref, int mask);
	public static void StencilFuncSeparate (CullFaceMode face, StencilFunction func, int ref, int mask);
	public static void StencilFuncSeparate (CullFaceMode face, StencilFunction func, int ref, uint mask);
	public static void StencilMaskSeparate (CullFaceMode face, uint mask);
	public static void StencilMaskSeparate (CullFaceMode face, int mask);
	public static void StencilOp (StencilOp fail, StencilOp zfail, StencilOp zpass);
	public static void StencilOpSeparate (CullFaceMode face, StencilOp fail, StencilOp zfail, StencilOp zpass);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, out T8 pixels);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, T8[0...,0...,0...] pixels);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, T8[0...,0...] pixels);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, T8[] pixels);
	public static void TexImage2D (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, System.IntPtr pixels);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, int* params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, int[] params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, int param);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, float* params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, float[] params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, float param);
	public static void TexSubImage2D (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, System.IntPtr pixels);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, T8[] pixels);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, T8[0...,0...] pixels);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, out T8 pixels);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, T8[0...,0...,0...] pixels);
	public static void VertexAttribPointer (int index, int size, VertexAttribPointerType type, bool normalized, int stride, int offset);
	public static void VertexAttribPointer (uint index, int size, VertexAttribPointerType type, bool normalized, int stride, int offset);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[] ptr);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...] ptr);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...,0...] ptr);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, out T5 ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[] ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...] ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...,0...] ptr);
	public static void VertexAttribPointer (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, System.IntPtr ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, out T5 ptr);
	public static void VertexAttribPointer (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, System.IntPtr ptr);
```

Obsoleted methods:

```
[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ActiveTexture (All texture);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindBuffer (All target, int buffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindBuffer (All target, uint buffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindFramebuffer (All target, int framebuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindFramebuffer (All target, uint framebuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindRenderbuffer (All target, uint renderbuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindRenderbuffer (All target, int renderbuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindTexture (All target, int texture);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindTexture (All target, uint texture);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlendEquation (All mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlendEquationSeparate (All modeRGB, All modeAlpha);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlendFunc (All sfactor, All dfactor);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlendFuncSeparate (All srcRGB, All dstRGB, All srcAlpha, All dstAlpha);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferData<T2> (All target, System.IntPtr size, out T2 data, All usage);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferData<T2> (All target, System.IntPtr size, T2[0...,0...,0...] data, All usage);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferData<T2> (All target, System.IntPtr size, T2[0...,0...] data, All usage);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferData<T2> (All target, System.IntPtr size, T2[] data, All usage);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferData (All target, System.IntPtr size, System.IntPtr data, All usage);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferSubData<T3> (All target, System.IntPtr offset, System.IntPtr size, out T3 data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferSubData<T3> (All target, System.IntPtr offset, System.IntPtr size, T3[0...,0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferSubData<T3> (All target, System.IntPtr offset, System.IntPtr size, T3[0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferSubData<T3> (All target, System.IntPtr offset, System.IntPtr size, T3[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferSubData (All target, System.IntPtr offset, System.IntPtr size, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static All CheckFramebufferStatus (All target);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, T7[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D (All target, int level, All internalformat, int width, int height, int border, int imageSize, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, T7[0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, out T7 data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, T7[0...,0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, out T8 data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, T8[0...,0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, T8[0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, T8[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CopyTexImage2D (All target, int level, All internalformat, int x, int y, int width, int height, int border);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CopyTexSubImage2D (All target, int level, int xoffset, int yoffset, int x, int y, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int CreateShader (All type);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CullFace (All mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DepthFunc (All func);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void Disable (All cap);

	[Obsolete ("Use the method in an extension subclass")]
	public static void DisableDriverControlQCOM (int driverControl);

	[Obsolete ("Use the method in an extension subclass")]
	public static void DisableDriverControlQCOM (uint driverControl);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawArrays (All mode, int first, int count);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements (All mode, int count, All type, System.IntPtr indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements<T3> (All mode, int count, All type, T3[] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements<T3> (All mode, int count, All type, T3[0...,0...] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements<T3> (All mode, int count, All type, T3[0...,0...,0...] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements<T3> (All mode, int count, All type, out T3 indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void Enable (All cap);

	[Obsolete ("Use the method in an extension subclass")]
	public static void EnableDriverControlQCOM (int driverControl);

	[Obsolete ("Use the method in an extension subclass")]
	public static void EnableDriverControlQCOM (uint driverControl);

	[Obsolete ("Use the method in an extension subclass")]
	public static void EndTilingQCOM (uint preserveMask);

	[Obsolete ("Use the method in an extension subclass")]
	public static void EndTilingQCOM (int preserveMask);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM (All target, System.IntPtr params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM<T1> (All target, T1[] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM<T1> (All target, T1[0...,0...] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM<T1> (All target, T1[0...,0...,0...] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBufferPointervQCOM<T1> (All target, out T1 params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (ref int buffers, int maxBuffers, ref int numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (uint* buffers, int maxBuffers, int* numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (ref uint buffers, int maxBuffers, ref int numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (uint[] buffers, int maxBuffers, int[] numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (int* buffers, int maxBuffers, int* numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetBuffersQCOM (int[] buffers, int maxBuffers, int[] numBuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (int[] framebuffers, int maxFramebuffers, int[] numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (ref int framebuffers, int maxFramebuffers, ref int numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (int* framebuffers, int maxFramebuffers, int* numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (uint[] framebuffers, int maxFramebuffers, int[] numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (ref uint framebuffers, int maxFramebuffers, ref int numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetFramebuffersQCOM (uint* framebuffers, int maxFramebuffers, int* numFramebuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (uint program, All shadertype, string source, int* length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (int program, All shadertype, string source, int[] length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (int program, All shadertype, string source, ref int length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (int program, All shadertype, string source, int* length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (uint program, All shadertype, string source, int[] length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramBinarySourceQCOM (uint program, All shadertype, string source, ref int length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (int[] programs, int maxPrograms, int[] numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (uint* programs, int maxPrograms, int* numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (ref uint programs, int maxPrograms, ref int numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (uint[] programs, int maxPrograms, int[] numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (int* programs, int maxPrograms, int* numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetProgramsQCOM (ref int programs, int maxPrograms, ref int numPrograms);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (uint* renderbuffers, int maxRenderbuffers, int* numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (int[] renderbuffers, int maxRenderbuffers, int[] numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (ref int renderbuffers, int maxRenderbuffers, ref int numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (int* renderbuffers, int maxRenderbuffers, int* numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (uint[] renderbuffers, int maxRenderbuffers, int[] numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetRenderbuffersQCOM (ref uint renderbuffers, int maxRenderbuffers, ref int numRenderbuffers);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (int[] shaders, int maxShaders, int[] numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (uint* shaders, int maxShaders, int* numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (ref uint shaders, int maxShaders, ref int numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (uint[] shaders, int maxShaders, int[] numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (int* shaders, int maxShaders, int* numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetShadersQCOM (ref int shaders, int maxShaders, ref int numShaders);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (uint texture, All face, int level, All pname, int* params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (int texture, All face, int level, All pname, int[] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (int texture, All face, int level, All pname, ref int params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (int texture, All face, int level, All pname, int* params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (uint texture, All face, int level, All pname, int[] params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexLevelParameterivQCOM (uint texture, All face, int level, All pname, ref int params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, System.IntPtr texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, out T10 texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...,0...] texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...] texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexSubImageQCOM<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[] texels);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (uint[] textures, int maxTextures, int[] numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (ref uint textures, int maxTextures, ref int numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (uint* textures, int maxTextures, int* numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (int* textures, int maxTextures, int* numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (ref int textures, int maxTextures, ref int numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtGetTexturesQCOM (int[] textures, int maxTextures, int[] numTextures);

	[Obsolete ("Use the method in an extension subclass")]
	public static bool ExtIsProgramBinaryQCOM (int program);

	[Obsolete ("Use the method in an extension subclass")]
	public static bool ExtIsProgramBinaryQCOM (uint program);

	[Obsolete ("Use the method in an extension subclass")]
	public static void ExtTexObjectStateOverrideiQCOM (All target, All pname, int param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferRenderbuffer (All target, All attachment, All renderbuffertarget, int renderbuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferRenderbuffer (All target, All attachment, All renderbuffertarget, uint renderbuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferTexture2D (All target, All attachment, All textarget, uint texture, int level);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferTexture2D (All target, All attachment, All textarget, int texture, int level);

	[Obsolete ("Use the method in an extension subclass")]
	public static void FramebufferTexture2DMultisampleIMG (All target, All attachment, All textarget, uint texture, int level, int samples);

	[Obsolete ("Use the method in an extension subclass")]
	public static void FramebufferTexture2DMultisampleIMG (All target, All attachment, All textarget, int texture, int level, int samples);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FrontFace (All mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GenerateMipmap (All target);

	[Obsolete]
	public static string GetActiveAttrib (int program, int index, out int size, out All type);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (int program, int index, int bufsize, out int length, out int size, out All type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (int program, int index, int bufsize, int[] length, int[] size, All[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (uint program, uint index, int bufsize, int* length, int* size, All* type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (int program, int index, int bufsize, int* length, int* size, All* type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (uint program, uint index, int bufsize, int[] length, int[] size, All[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (uint program, uint index, int bufsize, out int length, out int size, out All type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static string GetActiveUniform (int program, int uniformIndex, out int size, out All type);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniform (int program, int index, int bufsize, int[] length, int[] size, All[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniform (int program, int index, int bufsize, int* length, int* size, All* type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniform (uint program, uint index, int bufsize, int[] length, int[] size, All[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniform (uint program, uint index, int bufsize, out int length, out int size, out All type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniform (uint program, uint index, int bufsize, int* length, int* size, All* type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniform (int program, int index, int bufsize, out int length, out int size, out All type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int GetAttribLocation (int program, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int GetAttribLocation (uint program, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBoolean (All pname, out bool params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBoolean (All pname, bool[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBoolean (All pname, bool* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, int* params);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (int[] num, int size, int[] driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (int[] num, int size, uint[] driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (out int num, int size, out int driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (out int num, int size, out uint driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (int* num, int size, int* driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlsQCOM (int* num, int size, uint* driverControls);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (uint driverControl, int bufSize, int[] length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (int driverControl, int bufSize, int[] length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (int driverControl, int bufSize, out int length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (uint driverControl, int bufSize, out int length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (uint driverControl, int bufSize, int* length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the method in an extension subclass")]
	public static void GetDriverControlStringQCOM (int driverControl, int bufSize, int* length, System.Text.StringBuilder driverControlString);

	[Obsolete ("Use the GetErrorCode method, for compatability with Xamarin Android's OpenTK-1.0")]
	public static All GetError ();

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFloat (All pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFloat (All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFloat (All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFramebufferAttachmentParameter (All target, All attachment, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFramebufferAttachmentParameter (All target, All attachment, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFramebufferAttachmentParameter (All target, All attachment, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (int program, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (int program, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (int program, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (uint program, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (uint program, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (uint program, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetRenderbufferParameter (All target, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetRenderbufferParameter (All target, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetRenderbufferParameter (All target, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (int shader, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (int shader, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (int shader, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (uint shader, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (uint shader, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (uint shader, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShaderPrecisionFormat (All shadertype, All precisiontype, int[] range, int[] precision);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShaderPrecisionFormat (All shadertype, All precisiontype, out int range, out int precision);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShaderPrecisionFormat (All shadertype, All precisiontype, int* range, int* precision);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static string GetString (All name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int GetUniformLocation (int program, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int GetUniformLocation (uint program, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (int index, All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (int index, All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (int index, All pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (int index, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (int index, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (int index, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (uint index, All pname, T2[] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (uint index, All pname, out T2 pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (uint index, All pname, T2[0...,0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (uint index, All pname, T2[0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer (uint index, All pname, System.IntPtr pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (int index, All pname, out T2 pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer (int index, All pname, System.IntPtr pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (int index, All pname, T2[] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (int index, All pname, T2[0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (int index, All pname, T2[0...,0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void Hint (All target, All mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static bool IsEnabled (All cap);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void PixelStore (All pname, int param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, T6[0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, T6[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, out T6 pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, T6[] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels (int x, int y, int width, int height, All format, All type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void RenderbufferStorage (All target, All internalformat, int width, int height);

	[Obsolete ("Use the method in an extension subclass")]
	public static void RenderbufferStorageMultisampleIMG (All target, int samples, All internalformat, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint* shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint* shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint* shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint* shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int[] shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int[] shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int[] shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int[] shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, int[] shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, ref int shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, uint* shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int* shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int* shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int* shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int* shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, int* shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref int shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref int shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref int shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref int shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, uint[] shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref uint shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref uint shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref uint shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref uint shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, ref uint shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint[] shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint[] shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint[] shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint[] shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the method in an extension subclass")]
	public static void StartTilingQCOM (int x, int y, int width, int height, int preserveMask);

	[Obsolete ("Use the method in an extension subclass")]
	public static void StartTilingQCOM (uint x, uint y, uint width, uint height, uint preserveMask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilFunc (All func, int ref, uint mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilFunc (All func, int ref, int mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilFuncSeparate (All face, All func, int ref, int mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilFuncSeparate (All face, All func, int ref, uint mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilMaskSeparate (All face, int mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilMaskSeparate (All face, uint mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilOp (All fail, All zfail, All zpass);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilOpSeparate (All face, All fail, All zfail, All zpass);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, T8[0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D (All target, int level, int internalformat, int width, int height, int border, All format, All type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, T8[] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, out T8 pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, T8[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, int param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, float param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, out T8 pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, T8[0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, T8[] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, T8[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, T5[] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, T5[0...,0...] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, T5[0...,0...,0...] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, out T5 ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer (uint indx, int size, All type, bool normalized, int stride, System.IntPtr ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer (int indx, int size, All type, bool normalized, int stride, System.IntPtr ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, T5[] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, T5[0...,0...] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, T5[0...,0...,0...] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, out T5 ptr);
```

### New Type OpenTK.Graphics.ES20.Img

```
public static class Img {
	// methods
	public static void FramebufferTexture2DMultisample (All target, All attachment, All textarget, int texture, int level, int samples);
	public static void FramebufferTexture2DMultisample (All target, All attachment, All textarget, uint texture, int level, int samples);
	public static void RenderbufferStorageMultisample (All target, int samples, All internalformat, int width, int height);
}
```

### New Type OpenTK.Graphics.ES20.Qcom

```
public static class Qcom {
	// methods
	public static void DisableDriverControl (int driverControl);
	public static void DisableDriverControl (uint driverControl);
	public static void EnableDriverControl (int driverControl);
	public static void EnableDriverControl (uint driverControl);
	public static void EndTiling (uint preserveMask);
	public static void EndTiling (int preserveMask);
	public static void ExtGetBufferPointer<T1> (All target, out T1 params);
	public static void ExtGetBufferPointer<T1> (All target, T1[0...,0...,0...] params);
	public static void ExtGetBufferPointer<T1> (All target, T1[0...,0...] params);
	public static void ExtGetBufferPointer<T1> (All target, T1[] params);
	public static void ExtGetBufferPointer (All target, System.IntPtr params);
	public static void ExtGetBuffers (uint* buffers, int maxBuffers, int* numBuffers);
	public static void ExtGetBuffers (ref uint buffers, int maxBuffers, ref int numBuffers);
	public static void ExtGetBuffers (uint[] buffers, int maxBuffers, int[] numBuffers);
	public static void ExtGetBuffers (int* buffers, int maxBuffers, int* numBuffers);
	public static void ExtGetBuffers (ref int buffers, int maxBuffers, ref int numBuffers);
	public static void ExtGetBuffers (int[] buffers, int maxBuffers, int[] numBuffers);
	public static void ExtGetFramebuffers (uint* framebuffers, int maxFramebuffers, int* numFramebuffers);
	public static void ExtGetFramebuffers (ref uint framebuffers, int maxFramebuffers, ref int numFramebuffers);
	public static void ExtGetFramebuffers (uint[] framebuffers, int maxFramebuffers, int[] numFramebuffers);
	public static void ExtGetFramebuffers (int* framebuffers, int maxFramebuffers, int* numFramebuffers);
	public static void ExtGetFramebuffers (ref int framebuffers, int maxFramebuffers, ref int numFramebuffers);
	public static void ExtGetFramebuffers (int[] framebuffers, int maxFramebuffers, int[] numFramebuffers);
	public static void ExtGetProgram (ref int programs, int maxPrograms, ref int numPrograms);
	public static void ExtGetProgram (int* programs, int maxPrograms, int* numPrograms);
	public static void ExtGetProgram (uint[] programs, int maxPrograms, int[] numPrograms);
	public static void ExtGetProgram (ref uint programs, int maxPrograms, ref int numPrograms);
	public static void ExtGetProgram (uint* programs, int maxPrograms, int* numPrograms);
	public static void ExtGetProgram (int[] programs, int maxPrograms, int[] numPrograms);
	public static void ExtGetProgramBinarySource (int program, All shadertype, string source, int[] length);
	public static void ExtGetProgramBinarySource (int program, All shadertype, string source, ref int length);
	public static void ExtGetProgramBinarySource (int program, All shadertype, string source, int* length);
	public static void ExtGetProgramBinarySource (uint program, All shadertype, string source, int[] length);
	public static void ExtGetProgramBinarySource (uint program, All shadertype, string source, ref int length);
	public static void ExtGetProgramBinarySource (uint program, All shadertype, string source, int* length);
	public static void ExtGetRenderbuffers (uint* renderbuffers, int maxRenderbuffers, int* numRenderbuffers);
	public static void ExtGetRenderbuffers (ref uint renderbuffers, int maxRenderbuffers, ref int numRenderbuffers);
	public static void ExtGetRenderbuffers (uint[] renderbuffers, int maxRenderbuffers, int[] numRenderbuffers);
	public static void ExtGetRenderbuffers (int* renderbuffers, int maxRenderbuffers, int* numRenderbuffers);
	public static void ExtGetRenderbuffers (ref int renderbuffers, int maxRenderbuffers, ref int numRenderbuffers);
	public static void ExtGetRenderbuffers (int[] renderbuffers, int maxRenderbuffers, int[] numRenderbuffers);
	public static void ExtGetShaders (uint* shaders, int maxShaders, int* numShaders);
	public static void ExtGetShaders (ref uint shaders, int maxShaders, ref int numShaders);
	public static void ExtGetShaders (uint[] shaders, int maxShaders, int[] numShaders);
	public static void ExtGetShaders (int* shaders, int maxShaders, int* numShaders);
	public static void ExtGetShaders (ref int shaders, int maxShaders, ref int numShaders);
	public static void ExtGetShaders (int[] shaders, int maxShaders, int[] numShaders);
	public static void ExtGetTexLevelParameter (uint texture, All face, int level, All pname, int* params);
	public static void ExtGetTexLevelParameter (uint texture, All face, int level, All pname, ref int params);
	public static void ExtGetTexLevelParameter (uint texture, All face, int level, All pname, int[] params);
	public static void ExtGetTexLevelParameter (int texture, All face, int level, All pname, int* params);
	public static void ExtGetTexLevelParameter (int texture, All face, int level, All pname, ref int params);
	public static void ExtGetTexLevelParameter (int texture, All face, int level, All pname, int[] params);
	public static void ExtGetTexSubImage<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, out T10 texels);
	public static void ExtGetTexSubImage<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...,0...] texels);
	public static void ExtGetTexSubImage<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...] texels);
	public static void ExtGetTexSubImage<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[] texels);
	public static void ExtGetTexSubImage (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, System.IntPtr texels);
	public static void ExtGetTextures (uint* textures, int maxTextures, int* numTextures);
	public static void ExtGetTextures (ref uint textures, int maxTextures, ref int numTextures);
	public static void ExtGetTextures (uint[] textures, int maxTextures, int[] numTextures);
	public static void ExtGetTextures (int* textures, int maxTextures, int* numTextures);
	public static void ExtGetTextures (ref int textures, int maxTextures, ref int numTextures);
	public static void ExtGetTextures (int[] textures, int maxTextures, int[] numTextures);
	public static bool ExtIsProgramBinary (uint program);
	public static bool ExtIsProgramBinary (int program);
	public static void ExtTexObjectStateOverride (All target, All pname, int param);
	public static void GetDriverControl (int* num, int size, uint* driverControls);
	public static void GetDriverControl (int* num, int size, int* driverControls);
	public static void GetDriverControl (out int num, int size, out uint driverControls);
	public static void GetDriverControl (out int num, int size, out int driverControls);
	public static void GetDriverControl (int[] num, int size, uint[] driverControls);
	public static void GetDriverControl (int[] num, int size, int[] driverControls);
	public static void GetDriverControlString (uint driverControl, int bufSize, int* length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (uint driverControl, int bufSize, out int length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (uint driverControl, int bufSize, int[] length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (int driverControl, int bufSize, int* length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (int driverControl, int bufSize, out int length, System.Text.StringBuilder driverControlString);
	public static void GetDriverControlString (int driverControl, int bufSize, int[] length, System.Text.StringBuilder driverControlString);
	public static void StartTiling (int x, int y, int width, int height, int preserveMask);
	public static void StartTiling (uint x, uint y, uint width, uint height, uint preserveMask);
}
```

### Type Changed: OpenTK.Graphics.ES20.PixelType

Added value:

```
UnsignedByte = 5121,
```

### Type Changed: OpenTK.Graphics.ES20.StencilOp

Added value:

```
Zero = 0,
```

### Type Changed: OpenTK.Graphics.ES20.StringName

Added value:

```
ShadingLanguageVersion = 35724,
```

### Type Changed: OpenTK.Graphics.ES20.TextureMinFilter

Added values:

```
Linear = 9729,
	Nearest = 9728,
```

### Type Changed: OpenTK.Graphics.ES20.TextureTarget

Added value:

```
Texture2D = 3553,
```

### Type Changed: OpenTK.Graphics.ES20.Unknown

Added value:

```
ImgTextureFormatBgra8888 = 1,
```

### New Type OpenTK.Graphics.ES20.AmdCompressed3Dctexture

```
[Serializable]
public enum AmdCompressed3Dctexture {
	AmdCompressed3DcTexture = 1,
	Gl3DcXAmd = 34809,
	Gl3DcXyAmd = 34810,
}
```

### New Type OpenTK.Graphics.ES20.AmdCompressedAtctexture

```
[Serializable]
public enum AmdCompressedAtctexture {
	AmdCompressedAtcTexture = 1,
	AtcRgbaExplicitAlphaAmd = 35987,
	AtcRgbaInterpolatedAlphaAmd = 34798,
	AtcRgbAmd = 35986,
}
```

### New Type OpenTK.Graphics.ES20.AmdPerformanceMonitor

```
[Serializable]
public enum AmdPerformanceMonitor {
	AmdPerformanceMonitor = 1,
	CounterRangeAmd = 35777,
	CounterTypeAmd = 35776,
	PercentageAmd = 35779,
	PerfmonResultAmd = 35782,
	PerfmonResultAvailableAmd = 35780,
	PerfmonResultSizeAmd = 35781,
	UnsignedInt64Amd = 35778,
}
```

### New Type OpenTK.Graphics.ES20.AmdProgramBinaryZ400

```
[Serializable]
public enum AmdProgramBinaryZ400 {
	AmdProgramBinaryZ400 = 1,
	Z400BinaryAmd = 34624,
}
```

### New Type OpenTK.Graphics.ES20.BlendEquationMode

```
[Serializable]
public enum BlendEquationMode {
	FuncAdd = 32774,
	FuncReverseSubtract = 32779,
	FuncSubtract = 32778,
}
```

### New Type OpenTK.Graphics.ES20.BufferParameterName

```
[Serializable]
public enum BufferParameterName {
	BufferSize = 34660,
	BufferUsage = 34661,
}
```

### New Type OpenTK.Graphics.ES20.BufferTarget

```
[Serializable]
public enum BufferTarget {
	ArrayBuffer = 34962,
	ElementArrayBuffer = 34963,
}
```

### New Type OpenTK.Graphics.ES20.BufferUsage

```
[Serializable]
public enum BufferUsage {
	DynamicDraw = 35048,
	StaticDraw = 35044,
	StreamDraw = 35040,
}
```

### New Type OpenTK.Graphics.ES20.DepthFunction

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

### New Type OpenTK.Graphics.ES20.ExtBlendMinmax

```
[Serializable]
public enum ExtBlendMinmax {
	ExtBlendMinmax = 1,
	MaxExt = 32776,
	MinExt = 32775,
}
```

### New Type OpenTK.Graphics.ES20.ExtDiscardFramebuffer

```
[Serializable]
public enum ExtDiscardFramebuffer {
	ColorExt = 6144,
	DepthExt = 6145,
	ExtDiscardFramebuffer = 1,
	StencilExt = 6146,
}
```

### New Type OpenTK.Graphics.ES20.ExtReadFormatBgra

```
[Serializable]
public enum ExtReadFormatBgra {
	BgraExt = 32993,
	ExtReadFormatBgra = 1,
	UnsignedShort1555RevExt = 33638,
	UnsignedShort4444RevExt = 33637,
}
```

### New Type OpenTK.Graphics.ES20.ExtTextureCompressionDxt1

```
[Serializable]
public enum ExtTextureCompressionDxt1 {
	CompressedRgbaS3tcDxt1Ext = 33777,
	CompressedRgbS3tcDxt1Ext = 33776,
	ExtTextureCompressionDxt1 = 1,
}
```

### New Type OpenTK.Graphics.ES20.ExtTextureFilterAnisotropic

```
[Serializable]
public enum ExtTextureFilterAnisotropic {
	ExtTextureFilterAnisotropic = 1,
	MaxTextureMaxAnisotropyExt = 34047,
	TextureMaxAnisotropyExt = 34046,
}
```

### New Type OpenTK.Graphics.ES20.ExtTextureFormatBgra8888

```
[Serializable]
public enum ExtTextureFormatBgra8888 {
	BgraExt = 32993,
	ExtTextureFormatBgra8888 = 1,
}
```

### New Type OpenTK.Graphics.ES20.ExtTextureType2101010Rev

```
[Serializable]
public enum ExtTextureType2101010Rev {
	ExtTextureType2101010Rev = 1,
	UnsignedInt2101010RevExt = 33640,
}
```

### New Type OpenTK.Graphics.ES20.FramebufferErrorCode

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

### New Type OpenTK.Graphics.ES20.FramebufferParameterName

```
[Serializable]
public enum FramebufferParameterName {
	FramebufferAttachmentObjectName = 36049,
	FramebufferAttachmentObjectType = 36048,
	FramebufferAttachmentTextureCubeMapFace = 36051,
	FramebufferAttachmentTextureLevel = 36050,
}
```

### New Type OpenTK.Graphics.ES20.FramebufferSlot

```
[Serializable]
public enum FramebufferSlot {
	ColorAttachment0 = 36064,
	DepthAttachment = 36096,
	StencilAttachment = 36128,
}
```

### New Type OpenTK.Graphics.ES20.FramebufferTarget

```
[Serializable]
public enum FramebufferTarget {
	Framebuffer = 36160,
}
```

### New Type OpenTK.Graphics.ES20.ImgMultisampledRenderToTexture

```
[Serializable]
public enum ImgMultisampledRenderToTexture {
	FramebufferIncompleteMultisampleImg = 37172,
	ImgMultisampledRenderToTexture = 1,
	MaxSamplesImg = 37173,
	RenderbufferSamplesImg = 37171,
	TextureSamplesImg = 37174,
}
```

### New Type OpenTK.Graphics.ES20.ImgProgramBinary

```
[Serializable]
public enum ImgProgramBinary {
	ImgProgramBinary = 1,
	SgxProgramBinaryImg = 37168,
}
```

### New Type OpenTK.Graphics.ES20.ImgReadFormat

```
[Serializable]
public enum ImgReadFormat {
	BgraImg = 32993,
	ImgReadFormat = 1,
	UnsignedShort4444RevImg = 33637,
}
```

### New Type OpenTK.Graphics.ES20.ImgShaderBinary

```
[Serializable]
public enum ImgShaderBinary {
	ImgShaderBinary = 1,
	SgxBinaryImg = 35850,
}
```

### New Type OpenTK.Graphics.ES20.ImgTextureCompressionPvrtc

```
[Serializable]
public enum ImgTextureCompressionPvrtc {
	CompressedRgbaPvrtc2Bppv1Img = 35843,
	CompressedRgbaPvrtc4Bppv1Img = 35842,
	CompressedRgbPvrtc2Bppv1Img = 35841,
	CompressedRgbPvrtc4Bppv1Img = 35840,
	ImgTextureCompressionPvrtc = 1,
}
```

### New Type OpenTK.Graphics.ES20.NvCoverageSample

```
[Serializable]
public enum NvCoverageSample {
	CoverageAllFragmentsNv = 36565,
	CoverageAttachmentNv = 36562,
	CoverageAutomaticNv = 36567,
	CoverageBufferBitNv = 32768,
	CoverageBuffersNv = 36563,
	CoverageComponent4Nv = 36561,
	CoverageComponentNv = 36560,
	CoverageEdgeFragmentsNv = 36566,
	CoverageSamplesNv = 36564,
	NvCoverageSample = 1,
}
```

### New Type OpenTK.Graphics.ES20.NvDepthNonlinear

```
[Serializable]
public enum NvDepthNonlinear {
	DepthComponent16NonlinearNv = 36396,
	NvDepthNonlinear = 1,
}
```

### New Type OpenTK.Graphics.ES20.NvFence

```
[Serializable]
public enum NvFence {
	AllCompletedNv = 34034,
	FenceConditionNv = 34036,
	FenceStatusNv = 34035,
	NvFence = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesCompressedEtc1Rgb8Texture

```
[Serializable]
public enum OesCompressedEtc1Rgb8Texture {
	Etc1Rgb8Oes = 36196,
	OesCompressedEtc1Rgb8Texture = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesCompressedPalettedTexture

```
[Serializable]
public enum OesCompressedPalettedTexture {
	OesCompressedPalettedTexture = 1,
	Palette4R5G6B5Oes = 35730,
	Palette4Rgb5A1Oes = 35732,
	Palette4Rgb8Oes = 35728,
	Palette4Rgba4Oes = 35731,
	Palette4Rgba8Oes = 35729,
	Palette8R5G6B5Oes = 35735,
	Palette8Rgb5A1Oes = 35737,
	Palette8Rgb8Oes = 35733,
	Palette8Rgba4Oes = 35736,
	Palette8Rgba8Oes = 35734,
}
```

### New Type OpenTK.Graphics.ES20.OesDepth24

```
[Serializable]
public enum OesDepth24 {
	DepthComponent24Oes = 33190,
	OesDepth24 = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesDepth32

```
[Serializable]
public enum OesDepth32 {
	DepthComponent32Oes = 33191,
	OesDepth32 = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesDepthTexture

```
[Serializable]
public enum OesDepthTexture {
	OesDepthTexture = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesEglImage

```
[Serializable]
public enum OesEglImage {
	OesEglImage = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesEglImageExternal

```
[Serializable]
public enum OesEglImageExternal {
	OesEglImageExternal = 1,
	RequiredTextureImageUnitsOes = 36200,
	SamplerExternalOes = 36198,
	TextureBindingExternalOes = 36199,
	TextureExternalOes = 36197,
}
```

### New Type OpenTK.Graphics.ES20.OesElementIndexUint

```
[Serializable]
public enum OesElementIndexUint {
	OesElementIndexUint = 1,
	UnsignedInt = 5125,
}
```

### New Type OpenTK.Graphics.ES20.OesFboRenderMipmap

```
[Serializable]
public enum OesFboRenderMipmap {
	OesFboRenderMipmap = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesFragmentPrecisionHigh

```
[Serializable]
public enum OesFragmentPrecisionHigh {
	OesFragmentPrecisionHigh = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesGetProgramBinary

```
[Serializable]
public enum OesGetProgramBinary {
	NumProgramBinaryFormatsOes = 34814,
	OesGetProgramBinary = 1,
	ProgramBinaryFormatsOes = 34815,
	ProgramBinaryLengthOes = 34625,
}
```

### New Type OpenTK.Graphics.ES20.OesMapbuffer

```
[Serializable]
public enum OesMapbuffer {
	BufferAccessOes = 35003,
	BufferMappedOes = 35004,
	BufferMapPointerOes = 35005,
	OesMapbuffer = 1,
	WriteOnlyOes = 35001,
}
```

### New Type OpenTK.Graphics.ES20.OesPackedDepthStencil

```
[Serializable]
public enum OesPackedDepthStencil {
	Depth24Stencil8Oes = 35056,
	DepthStencilOes = 34041,
	OesPackedDepthStencil = 1,
	UnsignedInt248Oes = 34042,
}
```

### New Type OpenTK.Graphics.ES20.OesRgb8Rgba8

```
[Serializable]
public enum OesRgb8Rgba8 {
	OesRgb8Rgba8 = 1,
	Rgb8Oes = 32849,
	Rgba8Oes = 32856,
}
```

### New Type OpenTK.Graphics.ES20.OesStandardDerivatives

```
[Serializable]
public enum OesStandardDerivatives {
	FragmentShaderDerivativeHintOes = 35723,
	OesStandardDerivatives = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesStencil1

```
[Serializable]
public enum OesStencil1 {
	OesStencil1 = 1,
	StencilIndex1Oes = 36166,
}
```

### New Type OpenTK.Graphics.ES20.OesStencil4

```
[Serializable]
public enum OesStencil4 {
	OesStencil4 = 1,
	StencilIndex4Oes = 36167,
}
```

### New Type OpenTK.Graphics.ES20.OesTexture3D

```
[Serializable]
public enum OesTexture3D {
	FramebufferAttachmentTexture3DZoffsetOes = 36052,
	Max3DTextureSizeOes = 32883,
	OesTexture3D = 1,
	Sampler3DOes = 35679,
	Texture3DOes = 32879,
	TextureBinding3DOes = 32874,
	TextureWrapROes = 32882,
}
```

### New Type OpenTK.Graphics.ES20.OesTextureFloat

```
[Serializable]
public enum OesTextureFloat {
	OesTextureFloat = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesTextureFloatLinear

```
[Serializable]
public enum OesTextureFloatLinear {
	OesTextureFloatLinear = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesTextureHalfFloat

```
[Serializable]
public enum OesTextureHalfFloat {
	HalfFloatOes = 36193,
	OesTextureHalfFloat = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesTextureHalfFloatLinear

```
[Serializable]
public enum OesTextureHalfFloatLinear {
	OesTextureHalfFloatLinear = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesTextureNpot

```
[Serializable]
public enum OesTextureNpot {
	OesTextureNpot = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesVertexArrayObject

```
[Serializable]
public enum OesVertexArrayObject {
	OesVertexArrayObject = 1,
	VertexArrayBindingOes = 34229,
}
```

### New Type OpenTK.Graphics.ES20.OesVertexHalfFloat

```
[Serializable]
public enum OesVertexHalfFloat {
	OesVertexHalfFloat = 1,
}
```

### New Type OpenTK.Graphics.ES20.OesVertexType1010102

```
[Serializable]
public enum OesVertexType1010102 {
	Int1010102Oes = 36343,
	OesVertexType1010102 = 1,
	UnsignedInt1010102Oes = 36342,
}
```

### New Type OpenTK.Graphics.ES20.OpenGlEsCoreVersions

```
[Serializable]
public enum OpenGlEsCoreVersions {
	EsVersion20 = 1,
}
```

### New Type OpenTK.Graphics.ES20.PixelInternalFormat

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

### New Type OpenTK.Graphics.ES20.PixelStoreParameter

```
[Serializable]
public enum PixelStoreParameter {
	PackAlignment = 3333,
	UnpackAlignment = 3317,
}
```

### New Type OpenTK.Graphics.ES20.QcomDriverControl

```
[Serializable]
public enum QcomDriverControl {
	QcomDriverControl = 1,
}
```

### New Type OpenTK.Graphics.ES20.QcomExtendedGet

```
[Serializable]
public enum QcomExtendedGet {
	QcomExtendedGet = 1,
	StateRestore = 35804,
	TextureDepthQcom = 35796,
	TextureFormatQcom = 35798,
	TextureHeightQcom = 35795,
	TextureImageValidQcom = 35800,
	TextureInternalFormatQcom = 35797,
	TextureNumLevelsQcom = 35801,
	TextureObjectValidQcom = 35803,
	TextureTargetQcom = 35802,
	TextureTypeQcom = 35799,
	TextureWidthQcom = 35794,
}
```

### New Type OpenTK.Graphics.ES20.QcomExtendedGet2

```
[Serializable]
public enum QcomExtendedGet2 {
	QcomExtendedGet2 = 1,
}
```

### New Type OpenTK.Graphics.ES20.QcomPerfmonGlobalMode

```
[Serializable]
public enum QcomPerfmonGlobalMode {
	PerfmonGlobalModeQcom = 36768,
	QcomPerfmonGlobalMode = 1,
}
```

### New Type OpenTK.Graphics.ES20.QcomTiledRendering

```
[Serializable]
public enum QcomTiledRendering {
	ColorBufferBit0Qcom = 1,
	ColorBufferBit1Qcom = 2,
	ColorBufferBit2Qcom = 4,
	ColorBufferBit3Qcom = 8,
	ColorBufferBit4Qcom = 16,
	ColorBufferBit5Qcom = 32,
	ColorBufferBit6Qcom = 64,
	ColorBufferBit7Qcom = 128,
	DepthBufferBit0Qcom = 256,
	DepthBufferBit1Qcom = 512,
	DepthBufferBit2Qcom = 1024,
	DepthBufferBit3Qcom = 2048,
	DepthBufferBit4Qcom = 4096,
	DepthBufferBit5Qcom = 8192,
	DepthBufferBit6Qcom = 16384,
	DepthBufferBit7Qcom = 32768,
	MultisampleBufferBit0Qcom = 16777216,
	MultisampleBufferBit1Qcom = 33554432,
	MultisampleBufferBit2Qcom = 67108864,
	MultisampleBufferBit3Qcom = 134217728,
	MultisampleBufferBit4Qcom = 268435456,
	MultisampleBufferBit5Qcom = 536870912,
	MultisampleBufferBit6Qcom = 1073741824,
	MultisampleBufferBit7Qcom = -2147483648,
	QcomTiledRendering = 1,
	StencilBufferBit0Qcom = 65536,
	StencilBufferBit1Qcom = 131072,
	StencilBufferBit2Qcom = 262144,
	StencilBufferBit3Qcom = 524288,
	StencilBufferBit4Qcom = 1048576,
	StencilBufferBit5Qcom = 2097152,
	StencilBufferBit6Qcom = 4194304,
	StencilBufferBit7Qcom = 8388608,
}
```

### New Type OpenTK.Graphics.ES20.QcomWriteonlyRendering

```
[Serializable]
public enum QcomWriteonlyRendering {
	QcomWriteonlyRendering = 1,
	WriteonlyRenderingQcom = 34851,
}
```

### New Type OpenTK.Graphics.ES20.RenderbufferInternalFormat

```
[Serializable]
public enum RenderbufferInternalFormat {
	DepthComponent16 = 33189,
	Rgb565 = 36194,
	Rgb5A1 = 32855,
	Rgba4 = 32854,
	StencilIndex8 = 36168,
}
```

### New Type OpenTK.Graphics.ES20.RenderbufferParameterName

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
	RenderbufferStencilSize = 36181,
	RenderbufferWidth = 36162,
}
```

### New Type OpenTK.Graphics.ES20.RenderbufferTarget

```
[Serializable]
public enum RenderbufferTarget {
	Renderbuffer = 36161,
}
```

### New Type OpenTK.Graphics.ES20.ShaderBinaryFormat

```
[Serializable]
public enum ShaderBinaryFormat {
}
```

### New Type OpenTK.Graphics.ES20.ShaderPrecision

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

### New Type OpenTK.Graphics.ES20.ShaderType

```
[Serializable]
public enum ShaderType {
	FragmentShader = 35632,
	VertexShader = 35633,
}
```

### New Type OpenTK.Graphics.ES20.VertexAttribParameter

```
[Serializable]
public enum VertexAttribParameter {
	CurrentVertexAttrib = 34342,
	VertexAttribArrayBufferBinding = 34975,
	VertexAttribArrayEnabled = 34338,
	VertexAttribArrayNormalized = 34922,
	VertexAttribArraySize = 34339,
	VertexAttribArrayStride = 34340,
	VertexAttribArrayType = 34341,
}
```

### New Type OpenTK.Graphics.ES20.VertexAttribPointerParameter

```
[Serializable]
public enum VertexAttribPointerParameter {
	VertexAttribArrayPointer = 34373,
}
```

## Namespace OpenTK.Graphics.ES30

### Type Changed: OpenTK.Graphics.ES30.ActiveAttribType

Added values:

```
FloatMat2x3 = 35685,
	FloatMat2x4 = 35686,
	FloatMat3x2 = 35687,
	FloatMat3x4 = 35688,
	FloatMat4x2 = 35689,
	FloatMat4x3 = 35690,
	Int = 5124,
	IntVec2 = 35667,
	IntVec3 = 35668,
	IntVec4 = 35669,
	UnsignedInt = 5125,
	UnsignedIntVec2 = 36294,
	UnsignedIntVec3 = 36295,
	UnsignedIntVec4 = 36296,
```

### Type Changed: OpenTK.Graphics.ES30.ActiveUniformType

Added values:

```
FloatMat2x3 = 35685,
	FloatMat2x4 = 35686,
	FloatMat3x2 = 35687,
	FloatMat3x4 = 35688,
	FloatMat4x2 = 35689,
	FloatMat4x3 = 35690,
	IntSampler2D = 36298,
	IntSampler2DArray = 36303,
	IntSampler3D = 36299,
	IntSamplerCube = 36300,
	Sampler2DArray = 36289,
	Sampler2DArrayShadow = 36292,
	Sampler2DShadow = 35682,
	Sampler3D = 35679,
	SamplerBinding = 35097,
	SamplerCubeShadow = 36293,
	UnsignedInt = 5125,
	UnsignedIntSampler2D = 36306,
	UnsignedIntSampler2DArray = 36311,
	UnsignedIntSampler3D = 36307,
	UnsignedIntSamplerCube = 36308,
	UnsignedIntVec2 = 36294,
	UnsignedIntVec3 = 36295,
	UnsignedIntVec4 = 36296,
```

### Type Changed: OpenTK.Graphics.ES30.All

Added values:

```
BlendEquationRgb = 32777,
	CopyReadBufferBinding = 36662,
	CopyWriteBufferBinding = 36663,
	Depth32FStencil8 = 36013,
	DepthComponent32F = 36012,
	DrawFramebufferBinding = 36006,
	ImgTextureFormatBgra8888 = 1,
	StencilIndex = 6401,
```

### Type Changed: OpenTK.Graphics.ES30.BlendingFactorDest

Added values:

```
ConstantAlpha = 32771,
	ConstantColor = 32769,
	DstColor = 774,
	OneMinusConstantAlpha = 32772,
	OneMinusConstantColor = 32770,
	OneMinusDstColor = 775,
	SrcAlphaSaturate = 776,
```

### Type Changed: OpenTK.Graphics.ES30.BlendingFactorSrc

Added values:

```
ConstantAlpha = 32771,
	ConstantColor = 32769,
	DstAlpha = 772,
	One = 1,
	OneMinusConstantAlpha = 32772,
	OneMinusConstantColor = 32770,
	OneMinusDstAlpha = 773,
	OneMinusSrcAlpha = 771,
	OneMinusSrcColor = 769,
	SrcAlpha = 770,
	SrcColor = 768,
	Zero = 0,
```

### Type Changed: OpenTK.Graphics.ES30.DrawElementsType

Added value:

```
UnsignedInt = 5125,
```

### Type Changed: OpenTK.Graphics.ES30.EnableCap

Added values:

```
PrimitiveRestartFixedIndex = 36201,
	RasterizerDiscard = 35977,
```

### Type Changed: OpenTK.Graphics.ES30.ErrorCode

Added value:

```
InvalidFramebufferOperation = 1286,
```

### Type Changed: OpenTK.Graphics.ES30.FramebufferObject

Added value:

```
StencilIndex = 6401,
```

### Type Changed: OpenTK.Graphics.ES30.GetPName

Added values:

```
ActiveTexture = 34016,
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
	CompressedTextureFormats = 34467,
	CullFace = 2884,
	CurrentProgram = 35725,
	DepthTest = 2929,
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
	GenerateMipmapHint = 33170,
	ImplementationColorReadFormat = 35739,
	ImplementationColorReadType = 35738,
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
	MinorVersion = 33308,
	MinProgramTexelOffset = 35076,
	NumCompressedTextureFormats = 34466,
	NumExtensions = 33309,
	NumProgramBinaryFormats = 34814,
	NumShaderBinaryFormats = 36345,
	PackRowLength = 3330,
	PackSkipPixels = 3332,
	PackSkipRows = 3331,
	PixelPackBufferBinding = 35053,
	PixelUnpackBufferBinding = 35055,
	PolygonOffsetFill = 32823,
	PrimitiveRestartFixedIndex = 36201,
	ProgramBinaryFormats = 34815,
	ReadBuffer = 3074,
	ReadFramebufferBinding = 36010,
	RenderbufferBinding = 36007,
	SampleAlphaToCoverage = 32926,
	SampleCoverage = 32928,
	ScissorTest = 3089,
	ShaderBinaryFormats = 36344,
	ShaderCompiler = 36346,
	StencilTest = 2960,
	Texture2D = 3553,
	Texture3D = 32879,
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
	UnpackImageHeight = 32878,
	UnpackRowLength = 3314,
	UnpackSkipImages = 32877,
	UnpackSkipPixels = 3316,
	UnpackSkipRows = 3315,
	VertexArrayBinding = 34229,
```

### Type Changed: OpenTK.Graphics.ES30.GetTextureParameter

Added values:

```
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
```

### Type Changed: OpenTK.Graphics.ES30.GL

Added methods:

```
public static void ActiveTexture (TextureUnit texture);
	public static void BindBuffer (BufferTarget target, int buffer);
	public static void BindBuffer (BufferTarget target, uint buffer);
	public static void BindFramebuffer (FramebufferTarget target, uint framebuffer);
	public static void BindFramebuffer (FramebufferTarget target, int framebuffer);
	public static void BindRenderbuffer (RenderbufferTarget target, int renderbuffer);
	public static void BindRenderbuffer (RenderbufferTarget target, uint renderbuffer);
	public static void BindTexture (TextureTarget target, int texture);
	public static void BindTexture (TextureTarget target, uint texture);
	public static void BlendEquation (BlendEquationMode mode);
	public static void BlendEquationSeparate (BlendEquationMode modeRGB, BlendEquationMode modeAlpha);
	public static void BlendFunc (BlendingFactorSrc sfactor, BlendingFactorDest dfactor);
	public static void BlendFuncSeparate (BlendingFactorSrc srcRGB, BlendingFactorDest dstRGB, BlendingFactorSrc srcAlpha, BlendingFactorDest dstAlpha);
	public static void BufferData (BufferTarget target, System.IntPtr size, System.IntPtr data, BufferUsage usage);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, out T2 data, BufferUsage usage);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, T2[0...,0...,0...] data, BufferUsage usage);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, T2[0...,0...] data, BufferUsage usage);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, T2[] data, BufferUsage usage);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, T3[0...,0...,0...] data);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, out T3 data);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, T3[] data);
	public static void BufferSubData (BufferTarget target, System.IntPtr offset, System.IntPtr size, System.IntPtr data);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, T3[0...,0...] data);
	public static FramebufferErrorCode CheckFramebufferStatus (FramebufferTarget target);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, T7[0...,0...] data);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, T7[0...,0...,0...] data);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, out T7 data);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, T7[] data);
	public static void CompressedTexImage2D (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, System.IntPtr data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, T8[0...,0...,0...] data);
	public static void CompressedTexSubImage2D (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, System.IntPtr data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, out T8 data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, T8[] data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, T8[0...,0...] data);
	public static void CopyTexImage2D (TextureTarget target, int level, PixelInternalFormat internalformat, int x, int y, int width, int height, int border);
	public static void CopyTexSubImage2D (TextureTarget target, int level, int xoffset, int yoffset, int x, int y, int width, int height);
	public static int CreateShader (ShaderType type);
	public static void CullFace (CullFaceMode mode);
	public static void DeleteTexture (uint id);
	public static void DepthFunc (DepthFunction func);
	public static void Disable (EnableCap cap);
	public static void DrawArrays (BeginMode mode, int first, int count);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, T3[0...,0...,0...] indices);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, T3[] indices);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, out T3 indices);
	public static void DrawElements (BeginMode mode, int count, DrawElementsType type, System.IntPtr indices);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, T3[0...,0...] indices);
	public static void Enable (EnableCap cap);
	public static void FramebufferRenderbuffer (FramebufferTarget target, FramebufferSlot attachment, RenderbufferTarget renderbuffertarget, uint renderbuffer);
	public static void FramebufferRenderbuffer (FramebufferTarget target, FramebufferSlot attachment, RenderbufferTarget renderbuffertarget, int renderbuffer);
	public static void FramebufferTexture2D (FramebufferTarget target, FramebufferSlot attachment, TextureTarget textarget, uint texture, int level);
	public static void FramebufferTexture2D (FramebufferTarget target, FramebufferSlot attachment, TextureTarget textarget, int texture, int level);
	public static void FrontFace (FrontFaceDirection mode);
	public static void GenerateMipmap (TextureTarget target);
	public static void GetActiveAttrib (int program, int index, int bufsize, out int length, out int size, out ActiveAttribType type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, int* length, int* size, ActiveAttribType* type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, out int length, out int size, out ActiveAttribType type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, int[] length, int[] size, ActiveAttribType[] type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (int program, int index, int bufsize, int* length, int* size, ActiveAttribType* type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (int program, int index, int bufsize, int[] length, int[] size, ActiveAttribType[] type, System.Text.StringBuilder name);
	public static void GetActiveUniform (uint program, uint index, int bufsize, int[] length, int[] size, ActiveUniformType[] type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, int* length, int* size, ActiveUniformType* type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, out int length, out int size, out ActiveUniformType type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, int[] length, int[] size, ActiveUniformType[] type, System.Text.StringBuilder name);
	public static void GetActiveUniform (uint program, uint index, int bufsize, int* length, int* size, ActiveUniformType* type, System.Text.StringBuilder name);
	public static void GetActiveUniform (uint program, uint index, int bufsize, out int length, out int size, out ActiveUniformType type, System.Text.StringBuilder name);
	public static int GetAttribLocation (uint program, string name);
	public static int GetAttribLocation (int program, string name);
	public static void GetBoolean (GetPName pname, bool* params);
	public static void GetBoolean (GetPName pname, out bool params);
	public static void GetBoolean (GetPName pname, bool[] params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, long[] params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, out long params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, long* params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, int[] params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, out int params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, int* params);
	public static ErrorCode GetErrorCode ();
	public static void GetFloat (GetPName pname, float* params);
	public static void GetFloat (GetPName pname, out float params);
	public static void GetFloat (GetPName pname, float[] params);
	public static void GetFloat (GetPName pname, out OpenTK.Matrix4 matrix);
	public static void GetFloat (GetPName pname, out OpenTK.Vector4 vector);
	public static void GetFloat (GetPName pname, out OpenTK.Vector3 vector);
	public static void GetFloat (GetPName pname, out OpenTK.Vector2 vector);
	public static void GetFramebufferAttachmentParameter (FramebufferTarget target, FramebufferSlot attachment, FramebufferParameterName pname, out int params);
	public static void GetFramebufferAttachmentParameter (FramebufferTarget target, FramebufferSlot attachment, FramebufferParameterName pname, int[] params);
	public static void GetFramebufferAttachmentParameter (FramebufferTarget target, FramebufferSlot attachment, FramebufferParameterName pname, int* params);
	public static void GetInteger (GetPName pname, int* params);
	public static void GetInteger (GetPName pname, int[] params);
	public static void GetInteger (GetPName pname, out int params);
	public static void GetInteger (All target, uint index, long* data);
	public static void GetInteger (All target, uint index, out long data);
	public static void GetInteger (All target, uint index, long[] data);
	public static void GetInteger (All target, int index, long* data);
	public static void GetInteger (All target, int index, out long data);
	public static void GetInteger (All target, int index, long[] data);
	public static void GetProgram (int program, ProgramParameter pname, int[] params);
	public static void GetProgram (uint program, ProgramParameter pname, int* params);
	public static void GetProgram (uint program, ProgramParameter pname, out int params);
	public static void GetProgram (uint program, ProgramParameter pname, int[] params);
	public static void GetProgram (int program, ProgramParameter pname, int* params);
	public static void GetProgram (int program, ProgramParameter pname, out int params);
	public static void GetRenderbufferParameter (RenderbufferTarget target, RenderbufferParameterName pname, out int params);
	public static void GetRenderbufferParameter (RenderbufferTarget target, RenderbufferParameterName pname, int* params);
	public static void GetRenderbufferParameter (RenderbufferTarget target, RenderbufferParameterName pname, int[] params);
	public static void GetShader (uint shader, ShaderParameter pname, out int params);
	public static void GetShader (uint shader, ShaderParameter pname, int[] params);
	public static void GetShader (uint shader, ShaderParameter pname, int* params);
	public static void GetShader (int shader, ShaderParameter pname, int* params);
	public static void GetShader (int shader, ShaderParameter pname, out int params);
	public static void GetShader (int shader, ShaderParameter pname, int[] params);
	public static void GetShaderPrecisionFormat (ShaderType shadertype, ShaderPrecision precisiontype, int[] range, int[] precision);
	public static void GetShaderPrecisionFormat (ShaderType shadertype, ShaderPrecision precisiontype, out int range, out int precision);
	public static void GetShaderPrecisionFormat (ShaderType shadertype, ShaderPrecision precisiontype, int* range, int* precision);
	public static string GetString (StringName name, uint index);
	public static string GetString (StringName name);
	public static string GetString (StringName name, int index);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, int* params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, out int params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, int[] params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, float* params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, out float params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, float[] params);
	public static int GetUniformLocation (int program, string name);
	public static int GetUniformLocation (uint program, string name);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, float[] params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, out float params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, float* params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, float* params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, out float params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, float[] params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, out int params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, int[] params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, int* params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, out int params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, int[] params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, int* params);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, T2[0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, out T2 pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, T2[0...,0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, T2[0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, T2[] pointer);
	public static void GetVertexAttribPointer (uint index, VertexAttribPointerParameter pname, System.IntPtr pointer);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, out T2 pointer);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, T2[0...,0...,0...] pointer);
	public static void GetVertexAttribPointer (int index, VertexAttribPointerParameter pname, System.IntPtr pointer);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, T2[] pointer);
	public static void Hint (HintTarget target, HintMode mode);
	public static bool IsEnabled (EnableCap cap);
	public static void PixelStore (PixelStoreParameter pname, int param);
	public static void ReadPixels (int x, int y, int width, int height, PixelFormat format, PixelType type, System.IntPtr pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, T6[] pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, T6[0...,0...] pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, T6[0...,0...,0...] pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, out T6 pixels);
	public static void RenderbufferStorage (RenderbufferTarget target, RenderbufferInternalFormat internalformat, int width, int height);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary (int n, uint* shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary (int n, uint[] shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary (int n, ref uint shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary (int n, int* shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary (int n, int[] shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary (int n, ref int shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void StencilFunc (StencilFunction func, int ref, uint mask);
	public static void StencilFunc (StencilFunction func, int ref, int mask);
	public static void StencilFuncSeparate (CullFaceMode face, StencilFunction func, int ref, int mask);
	public static void StencilFuncSeparate (CullFaceMode face, StencilFunction func, int ref, uint mask);
	public static void StencilMaskSeparate (CullFaceMode face, uint mask);
	public static void StencilMaskSeparate (CullFaceMode face, int mask);
	public static void StencilOp (StencilOp fail, StencilOp zfail, StencilOp zpass);
	public static void StencilOpSeparate (CullFaceMode face, StencilOp fail, StencilOp zfail, StencilOp zpass);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, T8[] pixels);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, T8[0...,0...] pixels);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, T8[0...,0...,0...] pixels);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, out T8 pixels);
	public static void TexImage2D (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, System.IntPtr pixels);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, int* params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, int[] params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, int param);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, float* params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, float[] params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, float param);
	public static void TexSubImage2D (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, System.IntPtr pixels);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, out T8 pixels);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, T8[0...,0...,0...] pixels);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, T8[0...,0...] pixels);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, T8[] pixels);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, out T5 ptr);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...,0...] ptr);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...] ptr);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[] ptr);
	public static void VertexAttribPointer (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, System.IntPtr ptr);
	public static void VertexAttribPointer (uint index, int size, VertexAttribPointerType type, bool normalized, int stride, int offset);
	public static void VertexAttribPointer (int index, int size, VertexAttribPointerType type, bool normalized, int stride, int offset);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, out T5 ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...,0...] ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...] ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[] ptr);
	public static void VertexAttribPointer (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, System.IntPtr ptr);
```

Obsoleted methods:

```
[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ActiveTexture (All texture);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindBuffer (All target, int buffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindBuffer (All target, uint buffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindFramebuffer (All target, int framebuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindFramebuffer (All target, uint framebuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindRenderbuffer (All target, int renderbuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindRenderbuffer (All target, uint renderbuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindTexture (All target, int texture);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindTexture (All target, uint texture);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlendEquation (All mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlendEquationSeparate (All modeRGB, All modeAlpha);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlendFunc (All sfactor, All dfactor);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlendFuncSeparate (All srcRGB, All dstRGB, All srcAlpha, All dstAlpha);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferData<T2> (All target, System.IntPtr size, out T2 data, All usage);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferData<T2> (All target, System.IntPtr size, T2[0...,0...,0...] data, All usage);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferData (All target, System.IntPtr size, System.IntPtr data, All usage);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferData<T2> (All target, System.IntPtr size, T2[] data, All usage);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferData<T2> (All target, System.IntPtr size, T2[0...,0...] data, All usage);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferSubData<T3> (All target, System.IntPtr offset, System.IntPtr size, T3[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferSubData (All target, System.IntPtr offset, System.IntPtr size, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferSubData<T3> (All target, System.IntPtr offset, System.IntPtr size, T3[0...,0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferSubData<T3> (All target, System.IntPtr offset, System.IntPtr size, out T3 data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BufferSubData<T3> (All target, System.IntPtr offset, System.IntPtr size, T3[0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static All CheckFramebufferStatus (All target);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, out T7 data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, T7[0...,0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, T7[0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, T7[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D (All target, int level, All internalformat, int width, int height, int border, int imageSize, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, out T8 data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, T8[0...,0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, T8[0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, T8[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CopyTexImage2D (All target, int level, All internalformat, int x, int y, int width, int height, int border);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CopyTexSubImage2D (All target, int level, int xoffset, int yoffset, int x, int y, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int CreateShader (All type);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CullFace (All mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DepthFunc (All func);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void Disable (All cap);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawArrays (All mode, int first, int count);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements<T3> (All mode, int count, All type, T3[] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements<T3> (All mode, int count, All type, out T3 indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements<T3> (All mode, int count, All type, T3[0...,0...,0...] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements (All mode, int count, All type, System.IntPtr indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements<T3> (All mode, int count, All type, T3[0...,0...] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void Enable (All cap);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferRenderbuffer (All target, All attachment, All renderbuffertarget, uint renderbuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferRenderbuffer (All target, All attachment, All renderbuffertarget, int renderbuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferTexture2D (All target, All attachment, All textarget, uint texture, int level);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferTexture2D (All target, All attachment, All textarget, int texture, int level);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FrontFace (All mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GenerateMipmap (All target);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (int program, int index, int bufsize, int* length, int* size, All* type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (uint program, uint index, int bufsize, int[] length, int[] size, All[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (uint program, uint index, int bufsize, out int length, out int size, out All type, System.Text.StringBuilder name);

	[Obsolete]
	public static string GetActiveAttrib (int program, int index, out int size, out All type);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (int program, int index, int bufsize, int[] length, int[] size, All[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (uint program, uint index, int bufsize, int* length, int* size, All* type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (int program, int index, int bufsize, out int length, out int size, out All type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static string GetActiveUniform (int program, int uniformIndex, out int size, out All type);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniform (int program, int index, int bufsize, int[] length, int[] size, All[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniform (int program, int index, int bufsize, out int length, out int size, out All type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniform (int program, int index, int bufsize, int* length, int* size, All* type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniform (uint program, uint index, int bufsize, int[] length, int[] size, All[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniform (uint program, uint index, int bufsize, out int length, out int size, out All type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniform (uint program, uint index, int bufsize, int* length, int* size, All* type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int GetAttribLocation (int program, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int GetAttribLocation (uint program, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBoolean (All pname, bool[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBoolean (All pname, out bool params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBoolean (All pname, bool* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameteri64 (All target, All pname, long[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameteri64 (All target, All pname, out long params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameteri64 (All target, All pname, long* params);

	[Obsolete ("Use the GetErrorCode method, for compatability with Xamarin Android's OpenTK-1.0")]
	public static All GetError ();

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFloat (All pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFloat (All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFloat (All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFramebufferAttachmentParameter (All target, All attachment, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFramebufferAttachmentParameter (All target, All attachment, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFramebufferAttachmentParameter (All target, All attachment, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All target, uint index, out long data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All target, uint index, long[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All target, int index, long* data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All target, int index, out long data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All target, int index, long[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All target, uint index, long* data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (int program, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (int program, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (int program, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (uint program, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (uint program, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (uint program, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetRenderbufferParameter (All target, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetRenderbufferParameter (All target, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetRenderbufferParameter (All target, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (int shader, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (int shader, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (int shader, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (uint shader, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (uint shader, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (uint shader, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShaderPrecisionFormat (All shadertype, All precisiontype, out int range, out int precision);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShaderPrecisionFormat (All shadertype, All precisiontype, int[] range, int[] precision);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShaderPrecisionFormat (All shadertype, All precisiontype, int* range, int* precision);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static string GetString (All name, uint index);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static string GetString (All name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static string GetString (All name, int index);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int GetUniformLocation (int program, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int GetUniformLocation (uint program, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (int index, All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (int index, All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (int index, All pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (int index, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (int index, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (int index, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (uint index, All pname, T2[] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (int index, All pname, out T2 pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (uint index, All pname, T2[0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (uint index, All pname, T2[0...,0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (uint index, All pname, out T2 pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (int index, All pname, T2[0...,0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (int index, All pname, T2[0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (int index, All pname, T2[] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer (int index, All pname, System.IntPtr pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer (uint index, All pname, System.IntPtr pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void Hint (All target, All mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static bool IsEnabled (All cap);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void PixelStore (All pname, int param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels (int x, int y, int width, int height, All format, All type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, T6[] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, T6[0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, T6[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, out T6 pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void RenderbufferStorage (All target, All internalformat, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref uint shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref uint shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, uint* shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint* shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint* shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint* shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint* shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref uint shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, ref int shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int[] shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int[] shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int[] shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int[] shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, int[] shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref int shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref int shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, int* shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int* shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int* shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int* shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int* shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref int shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref int shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint[] shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, uint[] shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint[] shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint[] shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint[] shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, ref uint shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref uint shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilFunc (All func, int ref, int mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilFunc (All func, int ref, uint mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilFuncSeparate (All face, All func, int ref, int mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilFuncSeparate (All face, All func, int ref, uint mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilMaskSeparate (All face, int mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilMaskSeparate (All face, uint mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilOp (All fail, All zfail, All zpass);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilOpSeparate (All face, All fail, All zfail, All zpass);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D (All target, int level, int internalformat, int width, int height, int border, All format, All type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, T8[] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, T8[0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, T8[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, out T8 pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, int param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, float param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, out T8 pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, T8[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, T8[0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, T8[] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, T5[] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, T5[0...,0...] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, T5[0...,0...,0...] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, out T5 ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer (uint indx, int size, All type, bool normalized, int stride, System.IntPtr ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer (int indx, int size, All type, bool normalized, int stride, System.IntPtr ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, T5[] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, T5[0...,0...] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, T5[0...,0...,0...] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, out T5 ptr);
```

### Type Changed: OpenTK.Graphics.ES30.HintTarget

Added value:

```
FragmentShaderDerivativeHint = 35723,
```

### Type Changed: OpenTK.Graphics.ES30.PixelFormat

Added values:

```
DepthStencil = 34041,
	Red = 6403,
	RedInteger = 36244,
	Rg = 33319,
	RgbaInteger = 36249,
	RgbInteger = 36248,
	RgInteger = 33320,
```

### Type Changed: OpenTK.Graphics.ES30.PixelType

Added values:

```
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
```

### Type Changed: OpenTK.Graphics.ES30.ProgramParameter

Added value:

```
ProgramBinaryRetrievableHint = 33367,
```

### Type Changed: OpenTK.Graphics.ES30.StencilOp

Added value:

```
Zero = 0,
```

### Type Changed: OpenTK.Graphics.ES30.StringName

Added value:

```
ShadingLanguageVersion = 35724,
```

### Type Changed: OpenTK.Graphics.ES30.TextureMinFilter

Added values:

```
Linear = 9729,
	Nearest = 9728,
```

### Type Changed: OpenTK.Graphics.ES30.TextureParameterName

Added values:

```
TextureBaseLevel = 33084,
	TextureCompareFunc = 34893,
	TextureCompareMode = 34892,
	TextureMaxLevel = 33085,
	TextureMaxLod = 33083,
	TextureMinLod = 33082,
	TextureSwizzleA = 36421,
	TextureSwizzleB = 36420,
	TextureSwizzleG = 36419,
	TextureSwizzleR = 36418,
	TextureWrapR = 32882,
```

### Type Changed: OpenTK.Graphics.ES30.TextureTarget

Added values:

```
Texture2D = 3553,
	Texture2DArray = 35866,
	Texture3D = 32879,
```

### Type Changed: OpenTK.Graphics.ES30.Token

Added values:

```
CopyReadBufferBinding = 36662,
	CopyWriteBufferBinding = 36663,
	DrawFramebufferBinding = 36006,
	FramebufferBinding = 36006,
```

### Type Changed: OpenTK.Graphics.ES30.VertexAttribPointerType

Added values:

```
HalfFloat = 5131,
	Int = 5124,
	Int2101010Rev = 36255,
	UnsignedInt = 5125,
	UnsignedInt2101010Rev = 33640,
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

### New Type OpenTK.Graphics.ES30.OpenGlEsCoreVersions

```
[Serializable]
public enum OpenGlEsCoreVersions {
	EsVersion20 = 1,
	EsVersion30 = 1,
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

### New Type OpenTK.Graphics.ES30.ShaderBinaryFormat

```
[Serializable]
public enum ShaderBinaryFormat {
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

### New Type OpenTK.Graphics.ES30.ShaderType

```
[Serializable]
public enum ShaderType {
	FragmentShader = 35632,
	VertexShader = 35633,
}
```

### New Type OpenTK.Graphics.ES30.Unknown

```
[Serializable]
public enum Unknown {
	ImgTextureFormatBgra8888 = 1,
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

## Namespace OpenTK.Input

### Type Changed: OpenTK.Input.KeyboardState

Added properties:

```
public bool IsConnected { get; }
	public bool Item { get; }
```

Added methods:

```
public override bool Equals (object obj);
	public override int GetHashCode ();
	public static bool op_Equality (KeyboardState left, KeyboardState right);
	public static bool op_Inequality (KeyboardState left, KeyboardState right);
```

### Type Changed: OpenTK.Input.Mouse

Added methods:

```
public static MouseState GetState ();
	public static void SetPosition (double x, double y);
```

### Type Changed: OpenTK.Input.MouseState

Added properties:

```
public bool IsConnected { get; }
	public bool Item { get; }
	public ButtonState LeftButton { get; }
	public ButtonState MiddleButton { get; }
	public ButtonState RightButton { get; }
	public int ScrollWheelValue { get; }
	public int Wheel { get; }
	public float WheelPrecise { get; }
	public int X { get; }
	public ButtonState XButton1 { get; }
	public ButtonState XButton2 { get; }
	public int Y { get; }
```

Added methods:

```
public override bool Equals (object obj);
	public override int GetHashCode ();
	public bool IsButtonDown (MouseButton button);
	public bool IsButtonUp (MouseButton button);
	public static bool op_Equality (MouseState left, MouseState right);
	public static bool op_Inequality (MouseState left, MouseState right);
```

### New Type OpenTK.Input.ButtonState

```
[Serializable]
public enum ButtonState {
	Pressed = 1,
	Released = 0,
}
```
