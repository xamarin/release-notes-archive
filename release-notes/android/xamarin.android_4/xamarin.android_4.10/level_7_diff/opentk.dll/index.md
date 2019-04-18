---
id: 1D1E1E60-8E9D-4A70-B09D-9A27A4BCEA05
title: "OpenTK.dll"
---

# OpenTK.dll

## Namespace OpenTK.Graphics

### Type Changed: OpenTK.Graphics.GLContextVersion

Added values:

```
Gles3_0 = 4,
```

## New Namespace OpenTK.Graphics.ES30

### New Type OpenTK.Graphics.ES30.ActiveAttribType

```
[Serializable]
public enum ActiveAttribType {
	Float = 5126,
	FloatMat2 = 35674,
	FloatMat3 = 35675,
	FloatMat4 = 35676,
	FloatVec2 = 35664,
	FloatVec3 = 35665,
	FloatVec4 = 35666,
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
	FloatMat3 = 35675,
	FloatMat4 = 35676,
	FloatVec2 = 35664,
	FloatVec3 = 35665,
	FloatVec4 = 35666,
	Int = 5124,
	IntVec2 = 35667,
	IntVec3 = 35668,
	IntVec4 = 35669,
	Sampler2D = 35678,
	SamplerCube = 35680,
}
```

### New Type OpenTK.Graphics.ES30.All

```
[Serializable]
public enum All {
	ActiveAttributeMaxLength = 35722,
	ActiveAttributes = 35721,
	ActiveTexture = 34016,
	ActiveUniformBlockMaxNameLength = 35381,
	ActiveUniformBlocks = 35382,
	ActiveUniformMaxLength = 35719,
	ActiveUniforms = 35718,
	AliasedLineWidthRange = 33902,
	AliasedPointSizeRange = 33901,
	Alpha = 6406,
	AlphaBits = 3413,
	AlreadySignaled = 37146,
	Always = 519,
	AnySamplesPassed = 35887,
	AnySamplesPassedConservative = 36202,
	ArrayBuffer = 34962,
	ArrayBufferBinding = 34964,
	AttachedShaders = 35717,
	Back = 1029,
	Blend = 3042,
	BlendColor = 32773,
	BlendDstAlpha = 32970,
	BlendDstRgb = 32968,
	BlendEquation = 32777,
	BlendEquationAlpha = 34877,
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
	CompileStatus = 35713,
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
	CompressedTextureFormats = 34467,
	ConditionSatisfied = 37148,
	ConstantAlpha = 32771,
	ConstantColor = 32769,
	CopyReadBuffer = 36662,
	CopyWriteBuffer = 36663,
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
	DepthAttachment = 36096,
	DepthBits = 3414,
	DepthBufferBit = 256,
	DepthClearValue = 2931,
	DepthComponent = 6402,
	DepthComponent16 = 33189,
	DepthComponent24 = 33190,
	DepthComponent32f = 36012,
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
	Extensions = 7939,
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
	FragmentShaderDerivativeHint = 35723,
	Framebuffer = 36160,
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
	RgbaInteger = 36249,
	RgbInteger = 36248,
	RgInteger = 33320,
	SampleAlphaToCoverage = 32926,
	SampleBuffers = 32936,
	SampleCoverage = 32928,
	SampleCoverageInvert = 32939,
	SampleCoverageValue = 32938,
	Sampler2D = 35678,
	Sampler2DArray = 36289,
	Sampler2DArrayShadow = 36292,
	Sampler2DShadow = 35682,
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
	TextureCompareMode = 34892,
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
	UnsignedShort = 5123,
	UnsignedShort4444 = 32819,
	UnsignedShort5551 = 32820,
	UnsignedShort565 = 33635,
	ValidateStatus = 35715,
	Vendor = 7936,
	Version = 7938,
	VertexArrayBinding = 34229,
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
	DstAlpha = 772,
	One = 1,
	OneMinusDstAlpha = 773,
	OneMinusSrcAlpha = 771,
	OneMinusSrcColor = 769,
	SrcAlpha = 770,
	SrcColor = 768,
	Zero = 0,
}
```

### New Type OpenTK.Graphics.ES30.BlendingFactorSrc

```
[Serializable]
public enum BlendingFactorSrc {
	DstColor = 774,
	OneMinusDstColor = 775,
	SrcAlphaSaturate = 776,
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

### New Type OpenTK.Graphics.ES30.Boolean

```
[Serializable]
public enum Boolean {
	False = 0,
	True = 1,
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

### New Type OpenTK.Graphics.ES30.DrawElementsType

```
[Serializable]
public enum DrawElementsType {
	UnsignedByte = 5121,
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
	InvalidOperation = 1282,
	InvalidValue = 1281,
	NoError = 0,
	OutOfMemory = 1285,
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
	StencilIndex8 = 36168,
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

### New Type OpenTK.Graphics.ES30.GetPName

```
[Serializable]
public enum GetPName {
	AliasedLineWidthRange = 33902,
	AliasedPointSizeRange = 33901,
	AlphaBits = 3413,
	BlueBits = 3412,
	ColorClearValue = 3106,
	ColorWritemask = 3107,
	CullFaceMode = 2885,
	DepthBits = 3414,
	DepthClearValue = 2931,
	DepthFunc = 2932,
	DepthRange = 2928,
	DepthWritemask = 2930,
	FrontFace = 2886,
	GreenBits = 3411,
	LineWidth = 2849,
	MaxTextureSize = 3379,
	MaxViewportDims = 3386,
	PackAlignment = 3333,
	PolygonOffsetFactor = 32824,
	PolygonOffsetUnits = 10752,
	RedBits = 3410,
	SampleBuffers = 32936,
	SampleCoverageInvert = 32939,
	SampleCoverageValue = 32938,
	Samples = 32937,
	ScissorBox = 3088,
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
	StencilValueMask = 2963,
	StencilWritemask = 2968,
	SubpixelBits = 3408,
	TextureBinding2D = 32873,
	UnpackAlignment = 3317,
	Viewport = 2978,
}
```

### New Type OpenTK.Graphics.ES30.GetTextureParameter

```
[Serializable]
public enum GetTextureParameter {
	CompressedTextureFormats = 34467,
	NumCompressedTextureFormats = 34466,
}
```

### New Type OpenTK.Graphics.ES30.GL

```
public sealed class GL : OpenTK.Graphics.GraphicsBindingsBase {
	// constructors
	public GL ();
	// methods
	public static void ActiveTexture (All texture);
	public static void AttachShader (int program, int shader);
	public static void AttachShader (uint program, uint shader);
	public static void BeginQuery (All target, int id);
	public static void BeginQuery (All target, uint id);
	public static void BeginTransformFeedback (All primitiveMode);
	public static void BindAttribLocation (uint program, uint index, string name);
	public static void BindAttribLocation (int program, int index, string name);
	public static void BindBuffer (All target, int buffer);
	public static void BindBuffer (All target, uint buffer);
	public static void BindBufferBase (All target, int index, int buffer);
	public static void BindBufferBase (All target, uint index, uint buffer);
	public static void BindBufferRange (All target, uint index, uint buffer, System.IntPtr offset, System.IntPtr size);
	public static void BindBufferRange (All target, int index, int buffer, System.IntPtr offset, System.IntPtr size);
	public static void BindFramebuffer (All target, int framebuffer);
	public static void BindFramebuffer (All target, uint framebuffer);
	public static void BindRenderbuffer (All target, int renderbuffer);
	public static void BindRenderbuffer (All target, uint renderbuffer);
	public static void BindSampler (uint unit, uint sampler);
	public static void BindSampler (int unit, int sampler);
	public static void BindTexture (All target, int texture);
	public static void BindTexture (All target, uint texture);
	public static void BindTransformFeedback (All target, int id);
	public static void BindTransformFeedback (All target, uint id);
	public static void BindVertexArray (uint array);
	public static void BindVertexArray (int array);
	public static void BlendColor (float red, float green, float blue, float alpha);
	public static void BlendEquation (All mode);
	public static void BlendEquationSeparate (All modeRGB, All modeAlpha);
	public static void BlendFunc (All sfactor, All dfactor);
	public static void BlendFuncSeparate (All srcRGB, All dstRGB, All srcAlpha, All dstAlpha);
	public static void BlitFramebuffer (int srcX0, int srcY0, int srcX1, int srcY1, int dstX0, int dstY0, int dstX1, int dstY1, int mask, All filter);
	public static void BlitFramebuffer (int srcX0, int srcY0, int srcX1, int srcY1, int dstX0, int dstY0, int dstX1, int dstY1, uint mask, All filter);
	public static void BufferData<T2> (All target, System.IntPtr size, T2& data, All usage);
	public static void BufferData<T2> (All target, System.IntPtr size, T2[0...,0...,0...] data, All usage);
	public static void BufferData<T2> (All target, System.IntPtr size, T2[0...,0...] data, All usage);
	public static void BufferData<T2> (All target, System.IntPtr size, T2[] data, All usage);
	public static void BufferData (All target, System.IntPtr size, System.IntPtr data, All usage);
	public static void BufferSubData<T3> (All target, System.IntPtr offset, System.IntPtr size, T3& data);
	public static void BufferSubData<T3> (All target, System.IntPtr offset, System.IntPtr size, T3[0...,0...,0...] data);
	public static void BufferSubData<T3> (All target, System.IntPtr offset, System.IntPtr size, T3[0...,0...] data);
	public static void BufferSubData<T3> (All target, System.IntPtr offset, System.IntPtr size, T3[] data);
	public static void BufferSubData (All target, System.IntPtr offset, System.IntPtr size, System.IntPtr data);
	public static All CheckFramebufferStatus (All target);
	public static void Clear (ClearBufferMask mask);
	public static void ClearBuffer (All buffer, int drawbuffer, System.UInt32* value);
	public static void ClearBuffer (All buffer, int drawbuffer, System.UInt32& value);
	public static void ClearBuffer (All buffer, int drawbuffer, System.UInt32[] value);
	public static void ClearBuffer (All buffer, int drawbuffer, System.Int32* value);
	public static void ClearBuffer (All buffer, int drawbuffer, System.Int32& value);
	public static void ClearBuffer (All buffer, int drawbuffer, System.Int32[] value);
	public static void ClearBuffer (All buffer, int drawbuffer, System.Single* value);
	public static void ClearBuffer (All buffer, int drawbuffer, System.Single& value);
	public static void ClearBuffer (All buffer, int drawbuffer, System.Single[] value);
	public static void ClearBuffer (All buffer, int drawbuffer, float depth, int stencil);
	public static void ClearColor (float red, float green, float blue, float alpha);
	public static void ClearDepth (float depth);
	public static void ClearStencil (int s);
	public static All ClientWaitSync (System.IntPtr sync, int flags, long timeout);
	public static All ClientWaitSync (System.IntPtr sync, uint flags, ulong timeout);
	public static void ColorMask (bool red, bool green, bool blue, bool alpha);
	public static void CompileShader (uint shader);
	public static void CompileShader (int shader);
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, T7& data);
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, T7[0...,0...,0...] data);
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, T7[0...,0...] data);
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, T7[] data);
	public static void CompressedTexImage2D (All target, int level, All internalformat, int width, int height, int border, int imageSize, System.IntPtr data);
	public static void CompressedTexImage3D<T8> (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, T8& data);
	public static void CompressedTexImage3D<T8> (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, T8[0...,0...,0...] data);
	public static void CompressedTexImage3D<T8> (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, T8[0...,0...] data);
	public static void CompressedTexImage3D<T8> (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, T8[] data);
	public static void CompressedTexImage3D (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, System.IntPtr data);
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, T8& data);
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, T8[0...,0...,0...] data);
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, T8[0...,0...] data);
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, T8[] data);
	public static void CompressedTexSubImage2D (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, System.IntPtr data);
	public static void CompressedTexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, T10& data);
	public static void CompressedTexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, T10[0...,0...,0...] data);
	public static void CompressedTexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, T10[0...,0...] data);
	public static void CompressedTexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, T10[] data);
	public static void CompressedTexSubImage3D (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, System.IntPtr data);
	public static void CopyBufferSubData (All readTarget, All writeTarget, System.IntPtr readOffset, System.IntPtr writeOffset, System.IntPtr size);
	public static void CopyTexImage2D (All target, int level, All internalformat, int x, int y, int width, int height, int border);
	public static void CopyTexSubImage2D (All target, int level, int xoffset, int yoffset, int x, int y, int width, int height);
	public static void CopyTexSubImage3D (All target, int level, int xoffset, int yoffset, int zoffset, int x, int y, int width, int height);
	public static int CreateProgram ();
	public static int CreateShader (All type);
	public static void CullFace (All mode);
	public static void DeleteBuffers (int n, System.UInt32* buffers);
	public static void DeleteBuffers (int n, System.UInt32& buffers);
	public static void DeleteBuffers (int n, System.UInt32[] buffers);
	public static void DeleteBuffers (int n, System.Int32* buffers);
	public static void DeleteBuffers (int n, System.Int32& buffers);
	public static void DeleteBuffers (int n, System.Int32[] buffers);
	public static void DeleteFramebuffers (int n, System.UInt32* framebuffers);
	public static void DeleteFramebuffers (int n, System.UInt32& framebuffers);
	public static void DeleteFramebuffers (int n, System.UInt32[] framebuffers);
	public static void DeleteFramebuffers (int n, System.Int32* framebuffers);
	public static void DeleteFramebuffers (int n, System.Int32& framebuffers);
	public static void DeleteFramebuffers (int n, System.Int32[] framebuffers);
	public static void DeleteProgram (uint program);
	public static void DeleteProgram (int program);
	public static void DeleteQueries (int n, System.UInt32* ids);
	public static void DeleteQueries (int n, System.UInt32& ids);
	public static void DeleteQueries (int n, System.UInt32[] ids);
	public static void DeleteQueries (int n, System.Int32* ids);
	public static void DeleteQueries (int n, System.Int32& ids);
	public static void DeleteQueries (int n, System.Int32[] ids);
	public static void DeleteRenderbuffers (int n, System.UInt32* renderbuffers);
	public static void DeleteRenderbuffers (int n, System.UInt32& renderbuffers);
	public static void DeleteRenderbuffers (int n, System.UInt32[] renderbuffers);
	public static void DeleteRenderbuffers (int n, System.Int32* renderbuffers);
	public static void DeleteRenderbuffers (int n, System.Int32& renderbuffers);
	public static void DeleteRenderbuffers (int n, System.Int32[] renderbuffers);
	public static void DeleteSamplers (int count, System.UInt32* samplers);
	public static void DeleteSamplers (int count, System.UInt32& samplers);
	public static void DeleteSamplers (int count, System.UInt32[] samplers);
	public static void DeleteSamplers (int count, System.Int32* samplers);
	public static void DeleteSamplers (int count, System.Int32& samplers);
	public static void DeleteSamplers (int count, System.Int32[] samplers);
	public static void DeleteShader (uint shader);
	public static void DeleteShader (int shader);
	public static void DeleteSync (System.IntPtr sync);
	public static void DeleteTextures (int n, System.UInt32* textures);
	public static void DeleteTextures (int n, System.UInt32& textures);
	public static void DeleteTextures (int n, System.UInt32[] textures);
	public static void DeleteTextures (int n, System.Int32* textures);
	public static void DeleteTextures (int n, System.Int32& textures);
	public static void DeleteTextures (int n, System.Int32[] textures);
	public static void DeleteTransformFeedback (int n, System.UInt32* ids);
	public static void DeleteTransformFeedback (int n, System.UInt32& ids);
	public static void DeleteTransformFeedback (int n, System.UInt32[] ids);
	public static void DeleteTransformFeedback (int n, System.Int32* ids);
	public static void DeleteTransformFeedback (int n, System.Int32& ids);
	public static void DeleteTransformFeedback (int n, System.Int32[] ids);
	public static void DeleteVertexArrays (int n, System.UInt32* arrays);
	public static void DeleteVertexArrays (int n, System.UInt32& arrays);
	public static void DeleteVertexArrays (int n, System.UInt32[] arrays);
	public static void DeleteVertexArrays (int n, System.Int32[] arrays);
	public static void DeleteVertexArrays (int n, System.Int32& arrays);
	public static void DeleteVertexArrays (int n, System.Int32* arrays);
	public static void DepthFunc (All func);
	public static void DepthMask (bool flag);
	public static void DepthRange (float n, float f);
	public static void DetachShader (uint program, uint shader);
	public static void DetachShader (int program, int shader);
	public static void Disable (All cap);
	public static void DisableVertexAttribArray (int index);
	public static void DisableVertexAttribArray (uint index);
	public static void DrawArrays (All mode, int first, int count);
	public static void DrawArraysInstanced (All mode, int first, int count, int instanceCount);
	public static void DrawBuffers (int n, All[] bufs);
	public static void DrawBuffers (int n, All& bufs);
	public static void DrawBuffers (int n, All* bufs);
	public static void DrawElements<T3> (All mode, int count, All type, T3& indices);
	public static void DrawElements<T3> (All mode, int count, All type, T3[0...,0...,0...] indices);
	public static void DrawElements<T3> (All mode, int count, All type, T3[0...,0...] indices);
	public static void DrawElements<T3> (All mode, int count, All type, T3[] indices);
	public static void DrawElements (All mode, int count, All type, System.IntPtr indices);
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, T3& indices, int instanceCount);
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, T3[0...,0...,0...] indices, int instanceCount);
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, T3[0...,0...] indices, int instanceCount);
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, T3[] indices, int instanceCount);
	public static void DrawElementsInstanced (All mode, int count, All type, System.IntPtr indices, int instanceCount);
	public static void DrawRangeElements<T5> (All mode, uint start, uint end, int count, All type, T5[] indices);
	public static void DrawRangeElements<T5> (All mode, uint start, uint end, int count, All type, T5[0...,0...] indices);
	public static void DrawRangeElements<T5> (All mode, uint start, uint end, int count, All type, T5[0...,0...,0...] indices);
	public static void DrawRangeElements<T5> (All mode, uint start, uint end, int count, All type, T5& indices);
	public static void DrawRangeElements (All mode, uint start, uint end, int count, All type, System.IntPtr indices);
	public static void DrawRangeElements (All mode, int start, int end, int count, All type, System.IntPtr indices);
	public static void DrawRangeElements<T5> (All mode, int start, int end, int count, All type, T5[] indices);
	public static void DrawRangeElements<T5> (All mode, int start, int end, int count, All type, T5[0...,0...] indices);
	public static void DrawRangeElements<T5> (All mode, int start, int end, int count, All type, T5[0...,0...,0...] indices);
	public static void DrawRangeElements<T5> (All mode, int start, int end, int count, All type, T5& indices);
	public static void Enable (All cap);
	public static void EnableVertexAttribArray (uint index);
	public static void EnableVertexAttribArray (int index);
	public static void EndQuery (All target);
	public static void EndTransformFeedback ();
	public static System.IntPtr FenceSync (All condition, uint flags);
	public static System.IntPtr FenceSync (All condition, int flags);
	public static void Finish ();
	public static void Flush ();
	public static void FlushMappedBufferRange (All target, System.IntPtr offset, System.IntPtr length);
	public static void FramebufferRenderbuffer (All target, All attachment, All renderbuffertarget, int renderbuffer);
	public static void FramebufferRenderbuffer (All target, All attachment, All renderbuffertarget, uint renderbuffer);
	public static void FramebufferTexture2D (All target, All attachment, All textarget, uint texture, int level);
	public static void FramebufferTexture2D (All target, All attachment, All textarget, int texture, int level);
	public static void FramebufferTextureLayer (All target, All attachment, uint texture, int level, int layer);
	public static void FramebufferTextureLayer (All target, All attachment, int texture, int level, int layer);
	public static void FrontFace (All mode);
	public static void GenBuffers (int n, System.UInt32* buffers);
	public static void GenBuffers (int n, System.UInt32& buffers);
	public static void GenBuffers (int n, System.UInt32[] buffers);
	public static void GenBuffers (int n, System.Int32[] buffers);
	public static void GenBuffers (int n, System.Int32& buffers);
	public static void GenBuffers (int n, System.Int32* buffers);
	public static void GenerateMipmap (All target);
	public static void GenFramebuffers (int n, System.UInt32* framebuffers);
	public static void GenFramebuffers (int n, System.UInt32& framebuffers);
	public static void GenFramebuffers (int n, System.UInt32[] framebuffers);
	public static void GenFramebuffers (int n, System.Int32* framebuffers);
	public static void GenFramebuffers (int n, System.Int32& framebuffers);
	public static void GenFramebuffers (int n, System.Int32[] framebuffers);
	public static void GenQueries (int n, System.UInt32* ids);
	public static void GenQueries (int n, System.UInt32& ids);
	public static void GenQueries (int n, System.UInt32[] ids);
	public static void GenQueries (int n, System.Int32* ids);
	public static void GenQueries (int n, System.Int32& ids);
	public static void GenQueries (int n, System.Int32[] ids);
	public static void GenRenderbuffers (int n, System.UInt32* renderbuffers);
	public static void GenRenderbuffers (int n, System.UInt32& renderbuffers);
	public static void GenRenderbuffers (int n, System.UInt32[] renderbuffers);
	public static void GenRenderbuffers (int n, System.Int32* renderbuffers);
	public static void GenRenderbuffers (int n, System.Int32& renderbuffers);
	public static void GenRenderbuffers (int n, System.Int32[] renderbuffers);
	public static void GenSamplers (int count, System.UInt32* samplers);
	public static void GenSamplers (int count, System.UInt32& samplers);
	public static void GenSamplers (int count, System.UInt32[] samplers);
	public static void GenSamplers (int count, System.Int32* samplers);
	public static void GenSamplers (int count, System.Int32& samplers);
	public static void GenSamplers (int count, System.Int32[] samplers);
	public static void GenTextures (int n, System.UInt32* textures);
	public static void GenTextures (int n, System.UInt32& textures);
	public static void GenTextures (int n, System.UInt32[] textures);
	public static void GenTextures (int n, System.Int32* textures);
	public static void GenTextures (int n, System.Int32& textures);
	public static void GenTextures (int n, System.Int32[] textures);
	public static void GenTransformFeedback (int n, System.UInt32* ids);
	public static void GenTransformFeedback (int n, System.UInt32& ids);
	public static void GenTransformFeedback (int n, System.UInt32[] ids);
	public static void GenTransformFeedback (int n, System.Int32* ids);
	public static void GenTransformFeedback (int n, System.Int32& ids);
	public static void GenTransformFeedback (int n, System.Int32[] ids);
	public static void GenVertexArrays (int n, System.UInt32* arrays);
	public static void GenVertexArrays (int n, System.UInt32& arrays);
	public static void GenVertexArrays (int n, System.UInt32[] arrays);
	public static void GenVertexArrays (int n, System.Int32* arrays);
	public static void GenVertexArrays (int n, System.Int32& arrays);
	public static void GenVertexArrays (int n, System.Int32[] arrays);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, System.Int32* length, System.Int32* size, All* type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, System.Int32& length, System.Int32& size, All& type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, System.Int32[] length, System.Int32[] size, All[] type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (int program, int index, int bufsize, System.Int32* length, System.Int32* size, All* type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (int program, int index, int bufsize, System.Int32& length, System.Int32& size, All& type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (int program, int index, int bufsize, System.Int32[] length, System.Int32[] size, All[] type, System.Text.StringBuilder name);
	public static void GetActiveUniform (uint program, uint index, int bufsize, System.Int32* length, System.Int32* size, All* type, System.Text.StringBuilder name);
	public static void GetActiveUniform (uint program, uint index, int bufsize, System.Int32& length, System.Int32& size, All& type, System.Text.StringBuilder name);
	public static void GetActiveUniform (uint program, uint index, int bufsize, System.Int32[] length, System.Int32[] size, All[] type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, System.Int32* length, System.Int32* size, All* type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, System.Int32& length, System.Int32& size, All& type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, System.Int32[] length, System.Int32[] size, All[] type, System.Text.StringBuilder name);
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, All pname, System.Int32* params);
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, All pname, System.Int32& params);
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, All pname, System.Int32[] params);
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, All pname, System.Int32* params);
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, All pname, System.Int32& params);
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, All pname, System.Int32[] params);
	public static void GetActiveUniformBlockName (uint program, uint uniformBlockIndex, int bufSize, System.Int32* length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (uint program, uint uniformBlockIndex, int bufSize, System.Int32& length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (uint program, uint uniformBlockIndex, int bufSize, System.Int32[] length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (int program, int uniformBlockIndex, int bufSize, System.Int32* length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (int program, int uniformBlockIndex, int bufSize, System.Int32& length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (int program, int uniformBlockIndex, int bufSize, System.Int32[] length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniforms (uint program, int uniformCount, System.UInt32* uniformIndices, All pname, System.Int32* params);
	public static void GetActiveUniforms (uint program, int uniformCount, System.UInt32& uniformIndices, All pname, System.Int32& params);
	public static void GetActiveUniforms (uint program, int uniformCount, System.UInt32[] uniformIndices, All pname, System.Int32[] params);
	public static void GetActiveUniforms (int program, int uniformCount, System.Int32* uniformIndices, All pname, System.Int32* params);
	public static void GetActiveUniforms (int program, int uniformCount, System.Int32& uniformIndices, All pname, System.Int32& params);
	public static void GetActiveUniforms (int program, int uniformCount, System.Int32[] uniformIndices, All pname, System.Int32[] params);
	public static void GetAttachedShaders (uint program, int maxcount, System.Int32* count, System.UInt32* shaders);
	public static void GetAttachedShaders (uint program, int maxcount, System.Int32& count, System.UInt32& shaders);
	public static void GetAttachedShaders (uint program, int maxcount, System.Int32[] count, System.UInt32[] shaders);
	public static void GetAttachedShaders (int program, int maxcount, System.Int32[] count, System.Int32[] shaders);
	public static void GetAttachedShaders (int program, int maxcount, System.Int32& count, System.Int32& shaders);
	public static void GetAttachedShaders (int program, int maxcount, System.Int32* count, System.Int32* shaders);
	public static int GetAttribLocation (int program, System.Text.StringBuilder name);
	public static int GetAttribLocation (uint program, System.Text.StringBuilder name);
	public static void GetBoolean (All pname, System.Boolean* params);
	public static void GetBoolean (All pname, System.Boolean& params);
	public static void GetBoolean (All pname, System.Boolean[] params);
	public static void GetBufferParameter (All target, All pname, System.Int32* params);
	public static void GetBufferParameter (All target, All pname, System.Int32& params);
	public static void GetBufferParameter (All target, All pname, System.Int32[] params);
	public static void GetBufferParameteri64 (All target, All pname, System.Int64* params);
	public static void GetBufferParameteri64 (All target, All pname, System.Int64& params);
	public static void GetBufferParameteri64 (All target, All pname, System.Int64[] params);
	public static void GetBufferPointer<T2> (All target, All pname, T2& params);
	public static void GetBufferPointer<T2> (All target, All pname, T2[0...,0...,0...] params);
	public static void GetBufferPointer<T2> (All target, All pname, T2[0...,0...] params);
	public static void GetBufferPointer<T2> (All target, All pname, T2[] params);
	public static void GetBufferPointer (All target, All pname, System.IntPtr params);
	public static All GetError ();
	public static void GetFloat (All pname, System.Single* params);
	public static void GetFloat (All pname, System.Single& params);
	public static void GetFloat (All pname, System.Single[] params);
	public static int GetFragDataLocation (int program, System.Text.StringBuilder name);
	public static int GetFragDataLocation (uint program, System.Text.StringBuilder name);
	public static void GetFramebufferAttachmentParameter (All target, All attachment, All pname, System.Int32* params);
	public static void GetFramebufferAttachmentParameter (All target, All attachment, All pname, System.Int32& params);
	public static void GetFramebufferAttachmentParameter (All target, All attachment, All pname, System.Int32[] params);
	public static void GetInteger (All target, int index, System.Int32& data);
	public static void GetInteger (All target, int index, System.Int32* data);
	public static void GetInteger (All target, uint index, System.Int32[] data);
	public static void GetInteger (All target, uint index, System.Int32& data);
	public static void GetInteger (All target, uint index, System.Int32* data);
	public static void GetInteger (All pname, System.Int32[] params);
	public static void GetInteger (All pname, System.Int32& params);
	public static void GetInteger (All pname, System.Int32* params);
	public static void GetInteger (All target, int index, System.Int32[] data);
	public static void GetInteger64 (All target, int index, System.Int64[] data);
	public static void GetInteger64 (All target, int index, System.Int64& data);
	public static void GetInteger64 (All target, int index, System.Int64* data);
	public static void GetInteger64 (All target, uint index, System.Int64[] data);
	public static void GetInteger64 (All target, uint index, System.Int64& data);
	public static void GetInteger64 (All target, uint index, System.Int64* data);
	public static void GetInteger64 (All pname, System.Int64[] params);
	public static void GetInteger64 (All pname, System.Int64& params);
	public static void GetInteger64 (All pname, System.Int64* params);
	public static void GetInternalformat (All target, All internalformat, All pname, int bufSize, System.Int32* params);
	public static void GetInternalformat (All target, All internalformat, All pname, int bufSize, System.Int32& params);
	public static void GetInternalformat (All target, All internalformat, All pname, int bufSize, System.Int32[] params);
	public static void GetProgram (int program, All pname, System.Int32[] params);
	public static void GetProgram (int program, All pname, System.Int32& params);
	public static void GetProgram (int program, All pname, System.Int32* params);
	public static void GetProgram (uint program, All pname, System.Int32[] params);
	public static void GetProgram (uint program, All pname, System.Int32& params);
	public static void GetProgram (uint program, All pname, System.Int32* params);
	public static void GetProgramBinary<T4> (uint program, int bufSize, System.Int32& length, All& binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, System.Int32& length, All& binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, System.Int32& length, All& binaryFormat, T4[] binary);
	public static void GetProgramBinary (uint program, int bufSize, System.Int32& length, All& binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, System.Int32[] length, All[] binaryFormat, T4& binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, System.Int32& length, All& binaryFormat, T4& binary);
	public static void GetProgramBinary (uint program, int bufSize, System.Int32* length, All* binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, System.Int32* length, All* binaryFormat, T4[] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, System.Int32* length, All* binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, System.Int32* length, All* binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, System.Int32* length, All* binaryFormat, T4& binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, System.Int32[] length, All[] binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, System.Int32& length, All& binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, System.Int32& length, All& binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, System.Int32& length, All& binaryFormat, T4[] binary);
	public static void GetProgramBinary (int program, int bufSize, System.Int32[] length, All[] binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, System.Int32[] length, All[] binaryFormat, T4[] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, System.Int32[] length, All[] binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, System.Int32[] length, All[] binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, System.Int32[] length, All[] binaryFormat, T4& binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, System.Int32& length, All& binaryFormat, T4& binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, System.Int32[] length, All[] binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, System.Int32[] length, All[] binaryFormat, T4[] binary);
	public static void GetProgramBinary (uint program, int bufSize, System.Int32[] length, All[] binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, System.Int32* length, All* binaryFormat, T4& binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, System.Int32* length, All* binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, System.Int32* length, All* binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, System.Int32* length, All* binaryFormat, T4[] binary);
	public static void GetProgramBinary (int program, int bufSize, System.Int32* length, All* binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary (int program, int bufSize, System.Int32& length, All& binaryFormat, System.IntPtr binary);
	public static void GetProgramInfoLog (int program, int bufsize, System.Int32[] length, System.Text.StringBuilder infolog);
	public static void GetProgramInfoLog (int program, int bufsize, System.Int32& length, System.Text.StringBuilder infolog);
	public static void GetProgramInfoLog (int program, int bufsize, System.Int32* length, System.Text.StringBuilder infolog);
	public static void GetProgramInfoLog (uint program, int bufsize, System.Int32[] length, System.Text.StringBuilder infolog);
	public static void GetProgramInfoLog (uint program, int bufsize, System.Int32& length, System.Text.StringBuilder infolog);
	public static void GetProgramInfoLog (uint program, int bufsize, System.Int32* length, System.Text.StringBuilder infolog);
	public static void GetQuery (All target, All pname, System.Int32* params);
	public static void GetQuery (All target, All pname, System.Int32& params);
	public static void GetQuery (All target, All pname, System.Int32[] params);
	public static void GetQueryObject (uint id, All pname, System.UInt32* params);
	public static void GetQueryObject (uint id, All pname, System.UInt32& params);
	public static void GetQueryObject (uint id, All pname, System.UInt32[] params);
	public static void GetQueryObject (int id, All pname, System.Int32* params);
	public static void GetQueryObject (int id, All pname, System.Int32& params);
	public static void GetQueryObject (int id, All pname, System.Int32[] params);
	public static void GetRenderbufferParameter (All target, All pname, System.Int32* params);
	public static void GetRenderbufferParameter (All target, All pname, System.Int32& params);
	public static void GetRenderbufferParameter (All target, All pname, System.Int32[] params);
	public static void GetSamplerParameter (int sampler, All pname, System.Int32& params);
	public static void GetSamplerParameter (int sampler, All pname, System.Int32* params);
	public static void GetSamplerParameter (uint sampler, All pname, System.Int32[] params);
	public static void GetSamplerParameter (uint sampler, All pname, System.Int32& params);
	public static void GetSamplerParameter (uint sampler, All pname, System.Int32* params);
	public static void GetSamplerParameter (int sampler, All pname, System.Int32[] params);
	public static void GetSamplerParameter (int sampler, All pname, System.Single[] params);
	public static void GetSamplerParameter (int sampler, All pname, System.Single& params);
	public static void GetSamplerParameter (int sampler, All pname, System.Single* params);
	public static void GetSamplerParameter (uint sampler, All pname, System.Single[] params);
	public static void GetSamplerParameter (uint sampler, All pname, System.Single& params);
	public static void GetSamplerParameter (uint sampler, All pname, System.Single* params);
	public static void GetShader (int shader, All pname, System.Int32& params);
	public static void GetShader (int shader, All pname, System.Int32* params);
	public static void GetShader (uint shader, All pname, System.Int32[] params);
	public static void GetShader (uint shader, All pname, System.Int32& params);
	public static void GetShader (uint shader, All pname, System.Int32* params);
	public static void GetShader (int shader, All pname, System.Int32[] params);
	public static void GetShaderInfoLog (int shader, int bufsize, System.Int32[] length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (int shader, int bufsize, System.Int32& length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (int shader, int bufsize, System.Int32* length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (uint shader, int bufsize, System.Int32[] length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (uint shader, int bufsize, System.Int32& length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (uint shader, int bufsize, System.Int32* length, System.Text.StringBuilder infolog);
	public static void GetShaderPrecisionFormat (All shadertype, All precisiontype, System.Int32* range, System.Int32* precision);
	public static void GetShaderPrecisionFormat (All shadertype, All precisiontype, System.Int32& range, System.Int32& precision);
	public static void GetShaderPrecisionFormat (All shadertype, All precisiontype, System.Int32[] range, System.Int32[] precision);
	public static void GetShaderSource (uint shader, int bufsize, System.Int32* length, System.Text.StringBuilder source);
	public static void GetShaderSource (uint shader, int bufsize, System.Int32& length, System.Text.StringBuilder source);
	public static void GetShaderSource (uint shader, int bufsize, System.Int32[] length, System.Text.StringBuilder source);
	public static void GetShaderSource (int shader, int bufsize, System.Int32* length, System.Text.StringBuilder source);
	public static void GetShaderSource (int shader, int bufsize, System.Int32& length, System.Text.StringBuilder source);
	public static void GetShaderSource (int shader, int bufsize, System.Int32[] length, System.Text.StringBuilder source);
	public static string GetString (All name, uint index);
	public static string GetString (All name, int index);
	public static string GetString (All name);
	public static void GetSync (System.IntPtr sync, All pname, int bufSize, System.Int32* length, System.Int32* values);
	public static void GetSync (System.IntPtr sync, All pname, int bufSize, System.Int32& length, System.Int32& values);
	public static void GetSync (System.IntPtr sync, All pname, int bufSize, System.Int32[] length, System.Int32[] values);
	public static void GetTexParameter (All target, All pname, System.Int32* params);
	public static void GetTexParameter (All target, All pname, System.Int32& params);
	public static void GetTexParameter (All target, All pname, System.Int32[] params);
	public static void GetTexParameter (All target, All pname, System.Single* params);
	public static void GetTexParameter (All target, All pname, System.Single& params);
	public static void GetTexParameter (All target, All pname, System.Single[] params);
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, System.Int32* length, System.Int32* size, All* type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, System.Int32& length, System.Int32& size, All& type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, System.Int32[] length, System.Int32[] size, All[] type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, System.Int32* length, System.Int32* size, All* type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, System.Int32& length, System.Int32& size, All& type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, System.Int32[] length, System.Int32[] size, All[] type, System.Text.StringBuilder name);
	public static void GetUniform (uint program, int location, System.Int32[] params);
	public static void GetUniform (int program, int location, System.Int32* params);
	public static void GetUniform (int program, int location, System.Int32& params);
	public static void GetUniform (int program, int location, System.Int32[] params);
	public static void GetUniform (uint program, int location, System.Int32& params);
	public static void GetUniform (uint program, int location, System.Int32* params);
	public static void GetUniform (uint program, int location, System.UInt32[] params);
	public static void GetUniform (uint program, int location, System.UInt32& params);
	public static void GetUniform (uint program, int location, System.UInt32* params);
	public static void GetUniform (int program, int location, System.Single& params);
	public static void GetUniform (uint program, int location, System.Single& params);
	public static void GetUniform (uint program, int location, System.Single* params);
	public static void GetUniform (int program, int location, System.Single* params);
	public static void GetUniform (uint program, int location, System.Single[] params);
	public static void GetUniform (int program, int location, System.Single[] params);
	public static int GetUniformBlockIndex (int program, System.Text.StringBuilder uniformBlockName);
	public static int GetUniformBlockIndex (uint program, System.Text.StringBuilder uniformBlockName);
	public static void GetUniformIndices (int program, int uniformCount, System.Text.StringBuilder uniformNames, System.Int32& uniformIndices);
	public static void GetUniformIndices (int program, int uniformCount, System.Text.StringBuilder uniformNames, System.Int32* uniformIndices);
	public static void GetUniformIndices (uint program, int uniformCount, System.Text.StringBuilder uniformNames, System.UInt32[] uniformIndices);
	public static void GetUniformIndices (uint program, int uniformCount, System.Text.StringBuilder uniformNames, System.UInt32& uniformIndices);
	public static void GetUniformIndices (uint program, int uniformCount, System.Text.StringBuilder uniformNames, System.UInt32* uniformIndices);
	public static void GetUniformIndices (int program, int uniformCount, System.Text.StringBuilder uniformNames, System.Int32[] uniformIndices);
	public static int GetUniformLocation (uint program, System.Text.StringBuilder name);
	public static int GetUniformLocation (int program, System.Text.StringBuilder name);
	public static void GetVertexAttrib (uint index, All pname, System.Int32& params);
	public static void GetVertexAttrib (uint index, All pname, System.Int32[] params);
	public static void GetVertexAttrib (int index, All pname, System.Int32* params);
	public static void GetVertexAttrib (int index, All pname, System.Int32& params);
	public static void GetVertexAttrib (int index, All pname, System.Int32[] params);
	public static void GetVertexAttrib (uint index, All pname, System.Int32* params);
	public static void GetVertexAttrib (int index, All pname, System.Single[] params);
	public static void GetVertexAttrib (int index, All pname, System.Single& params);
	public static void GetVertexAttrib (int index, All pname, System.Single* params);
	public static void GetVertexAttrib (uint index, All pname, System.Single[] params);
	public static void GetVertexAttrib (uint index, All pname, System.Single& params);
	public static void GetVertexAttrib (uint index, All pname, System.Single* params);
	public static void GetVertexAttribI (uint index, All pname, System.UInt32* params);
	public static void GetVertexAttribI (uint index, All pname, System.UInt32& params);
	public static void GetVertexAttribI (int index, All pname, System.Int32[] params);
	public static void GetVertexAttribI (int index, All pname, System.Int32& params);
	public static void GetVertexAttribI (int index, All pname, System.Int32* params);
	public static void GetVertexAttribI (uint index, All pname, System.Int32[] params);
	public static void GetVertexAttribI (uint index, All pname, System.Int32& params);
	public static void GetVertexAttribI (uint index, All pname, System.Int32* params);
	public static void GetVertexAttribI (uint index, All pname, System.UInt32[] params);
	public static void GetVertexAttribPointer<T2> (uint index, All pname, T2[] pointer);
	public static void GetVertexAttribPointer<T2> (uint index, All pname, T2[0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (uint index, All pname, T2[0...,0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (uint index, All pname, T2& pointer);
	public static void GetVertexAttribPointer (uint index, All pname, System.IntPtr pointer);
	public static void GetVertexAttribPointer<T2> (int index, All pname, T2& pointer);
	public static void GetVertexAttribPointer<T2> (int index, All pname, T2[0...,0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (int index, All pname, T2[0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (int index, All pname, T2[] pointer);
	public static void GetVertexAttribPointer (int index, All pname, System.IntPtr pointer);
	public static void Hint (All target, All mode);
	public static void InvalidateFramebuffer (All target, int numAttachments, All* attachments);
	public static void InvalidateFramebuffer (All target, int numAttachments, All& attachments);
	public static void InvalidateFramebuffer (All target, int numAttachments, All[] attachments);
	public static void InvalidateSubFramebuffer (All target, int numAttachments, All[] attachments, int x, int y, int width, int height);
	public static void InvalidateSubFramebuffer (All target, int numAttachments, All& attachments, int x, int y, int width, int height);
	public static void InvalidateSubFramebuffer (All target, int numAttachments, All* attachments, int x, int y, int width, int height);
	public static bool IsBuffer (uint buffer);
	public static bool IsBuffer (int buffer);
	public static bool IsEnabled (All cap);
	public static bool IsFramebuffer (int framebuffer);
	public static bool IsFramebuffer (uint framebuffer);
	public static bool IsProgram (uint program);
	public static bool IsProgram (int program);
	public static bool IsQuery (int id);
	public static bool IsQuery (uint id);
	public static bool IsRenderbuffer (int renderbuffer);
	public static bool IsRenderbuffer (uint renderbuffer);
	public static bool IsSampler (uint sampler);
	public static bool IsSampler (int sampler);
	public static bool IsShader (int shader);
	public static bool IsShader (uint shader);
	public static bool IsSync (System.IntPtr sync);
	public static bool IsTexture (uint texture);
	public static bool IsTexture (int texture);
	public static bool IsTransformFeedback (uint id);
	public static bool IsTransformFeedback (int id);
	public static bool IsVertexArray (int array);
	public static bool IsVertexArray (uint array);
	public static void LineWidth (float width);
	public static void LinkProgram (uint program);
	public static void LinkProgram (int program);
	public static System.IntPtr MapBufferRange (All target, System.IntPtr offset, System.IntPtr length, int access);
	public static System.IntPtr MapBufferRange (All target, System.IntPtr offset, System.IntPtr length, uint access);
	public static void PauseTransformFeedback ();
	public static void PixelStore (All pname, int param);
	public static void PolygonOffset (float factor, float units);
	public static void ProgramBinary<T2> (uint program, All binaryFormat, T2& binary, int length);
	public static void ProgramBinary<T2> (uint program, All binaryFormat, T2[0...,0...,0...] binary, int length);
	public static void ProgramBinary<T2> (uint program, All binaryFormat, T2[0...,0...] binary, int length);
	public static void ProgramBinary<T2> (uint program, All binaryFormat, T2[] binary, int length);
	public static void ProgramBinary (uint program, All binaryFormat, System.IntPtr binary, int length);
	public static void ProgramBinary<T2> (int program, All binaryFormat, T2& binary, int length);
	public static void ProgramBinary<T2> (int program, All binaryFormat, T2[0...,0...,0...] binary, int length);
	public static void ProgramBinary<T2> (int program, All binaryFormat, T2[0...,0...] binary, int length);
	public static void ProgramBinary<T2> (int program, All binaryFormat, T2[] binary, int length);
	public static void ProgramBinary (int program, All binaryFormat, System.IntPtr binary, int length);
	public static void ProgramParameter (uint program, All pname, int value);
	public static void ProgramParameter (int program, All pname, int value);
	public static void ReadBuffer (All mode);
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, T6& pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, T6[0...,0...,0...] pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, T6[0...,0...] pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, T6[] pixels);
	public static void ReadPixels (int x, int y, int width, int height, All format, All type, System.IntPtr pixels);
	public static void ReleaseShaderCompiler ();
	public static void RenderbufferStorage (All target, All internalformat, int width, int height);
	public static void RenderbufferStorageMultisample (All target, int samples, All internalformat, int width, int height);
	public static void ResumeTransformFeedback ();
	public static void SampleCoverage (float value, bool invert);
	public static void SamplerParameter (uint sampler, All pname, int param);
	public static void SamplerParameter (int sampler, All pname, System.Int32[] param);
	public static void SamplerParameter (int sampler, All pname, System.Int32* param);
	public static void SamplerParameter (uint sampler, All pname, System.Int32[] param);
	public static void SamplerParameter (uint sampler, All pname, System.Int32* param);
	public static void SamplerParameter (int sampler, All pname, int param);
	public static void SamplerParameter (int sampler, All pname, float param);
	public static void SamplerParameter (uint sampler, All pname, float param);
	public static void SamplerParameter (int sampler, All pname, System.Single[] param);
	public static void SamplerParameter (int sampler, All pname, System.Single* param);
	public static void SamplerParameter (uint sampler, All pname, System.Single[] param);
	public static void SamplerParameter (uint sampler, All pname, System.Single* param);
	public static void Scissor (int x, int y, int width, int height);
	public static void ShaderBinary<T3> (int n, System.UInt32& shaders, All binaryformat, T3[] binary, int length);
	public static void ShaderBinary (int n, System.UInt32& shaders, All binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, System.UInt32[] shaders, All binaryformat, T3& binary, int length);
	public static void ShaderBinary<T3> (int n, System.UInt32[] shaders, All binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, System.UInt32[] shaders, All binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, System.UInt32[] shaders, All binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, System.UInt32& shaders, All binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, System.UInt32* shaders, All binaryformat, T3& binary, int length);
	public static void ShaderBinary<T3> (int n, System.UInt32* shaders, All binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, System.UInt32* shaders, All binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, System.UInt32* shaders, All binaryformat, T3[] binary, int length);
	public static void ShaderBinary (int n, System.UInt32* shaders, All binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, System.UInt32& shaders, All binaryformat, T3& binary, int length);
	public static void ShaderBinary<T3> (int n, System.UInt32& shaders, All binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary (int n, System.UInt32[] shaders, All binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, System.Int32& shaders, All binaryformat, T3[] binary, int length);
	public static void ShaderBinary (int n, System.Int32& shaders, All binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, System.Int32[] shaders, All binaryformat, T3& binary, int length);
	public static void ShaderBinary<T3> (int n, System.Int32[] shaders, All binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, System.Int32[] shaders, All binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, System.Int32[] shaders, All binaryformat, T3[] binary, int length);
	public static void ShaderBinary (int n, System.Int32[] shaders, All binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, System.Int32& shaders, All binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, System.Int32* shaders, All binaryformat, T3& binary, int length);
	public static void ShaderBinary<T3> (int n, System.Int32* shaders, All binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, System.Int32* shaders, All binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, System.Int32* shaders, All binaryformat, T3[] binary, int length);
	public static void ShaderBinary (int n, System.Int32* shaders, All binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, System.Int32& shaders, All binaryformat, T3& binary, int length);
	public static void ShaderBinary<T3> (int n, System.Int32& shaders, All binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderSource (uint shader, int count, System.String[] string, System.Int32* length);
	public static void ShaderSource (uint shader, int count, System.String[] string, System.Int32& length);
	public static void ShaderSource (uint shader, int count, System.String[] string, System.Int32[] length);
	public static void ShaderSource (int shader, int count, System.String[] string, System.Int32* length);
	public static void ShaderSource (int shader, int count, System.String[] string, System.Int32& length);
	public static void ShaderSource (int shader, int count, System.String[] string, System.Int32[] length);
	public static void StencilFunc (All func, int ref, int mask);
	public static void StencilFunc (All func, int ref, uint mask);
	public static void StencilFuncSeparate (All face, All func, int ref, uint mask);
	public static void StencilFuncSeparate (All face, All func, int ref, int mask);
	public static void StencilMask (uint mask);
	public static void StencilMask (int mask);
	public static void StencilMaskSeparate (All face, int mask);
	public static void StencilMaskSeparate (All face, uint mask);
	public static void StencilOp (All fail, All zfail, All zpass);
	public static void StencilOpSeparate (All face, All fail, All zfail, All zpass);
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, T8& pixels);
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, T8[0...,0...,0...] pixels);
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, T8[0...,0...] pixels);
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, T8[] pixels);
	public static void TexImage2D (All target, int level, int internalformat, int width, int height, int border, All format, All type, System.IntPtr pixels);
	public static void TexImage3D<T9> (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, T9& pixels);
	public static void TexImage3D<T9> (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, T9[0...,0...,0...] pixels);
	public static void TexImage3D<T9> (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, T9[0...,0...] pixels);
	public static void TexImage3D<T9> (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, T9[] pixels);
	public static void TexImage3D (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, System.IntPtr pixels);
	public static void TexParameter (All target, All pname, System.Int32* params);
	public static void TexParameter (All target, All pname, System.Int32[] params);
	public static void TexParameter (All target, All pname, int param);
	public static void TexParameter (All target, All pname, System.Single* params);
	public static void TexParameter (All target, All pname, System.Single[] params);
	public static void TexParameter (All target, All pname, float param);
	public static void TexStorage2D (All target, int levels, All internalformat, int width, int height);
	public static void TexStorage3D (All target, int levels, All internalformat, int width, int height, int depth);
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, T8& pixels);
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, T8[0...,0...,0...] pixels);
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, T8[0...,0...] pixels);
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, T8[] pixels);
	public static void TexSubImage2D (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, System.IntPtr pixels);
	public static void TexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10& pixels);
	public static void TexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...,0...] pixels);
	public static void TexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...] pixels);
	public static void TexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[] pixels);
	public static void TexSubImage3D (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, System.IntPtr pixels);
	public static void TransformFeedbackVaryings (uint program, int count, string varyings, All bufferMode);
	public static void TransformFeedbackVaryings (int program, int count, string varyings, All bufferMode);
	public static void Uniform1 (int location, int count, System.Int32* v);
	public static void Uniform1 (int location, uint v0);
	public static void Uniform1 (int location, int count, System.UInt32[] value);
	public static void Uniform1 (int location, int count, System.UInt32& value);
	public static void Uniform1 (int location, int count, System.UInt32* value);
	public static void Uniform1 (int location, int count, System.Int32& v);
	public static void Uniform1 (int location, float x);
	public static void Uniform1 (int location, int count, System.Single[] v);
	public static void Uniform1 (int location, int count, System.Single& v);
	public static void Uniform1 (int location, int count, System.Single* v);
	public static void Uniform1 (int location, int x);
	public static void Uniform1 (int location, int count, System.Int32[] v);
	public static void Uniform2 (int location, int count, System.Int32* v);
	public static void Uniform2 (int location, uint v0, uint v1);
	public static void Uniform2 (int location, int count, System.UInt32[] value);
	public static void Uniform2 (int location, int count, System.UInt32& value);
	public static void Uniform2 (int location, int count, System.UInt32* value);
	public static void Uniform2 (int location, int count, System.Int32[] v);
	public static void Uniform2 (int location, float x, float y);
	public static void Uniform2 (int location, int count, System.Single[] v);
	public static void Uniform2 (int location, int count, System.Single& v);
	public static void Uniform2 (int location, int count, System.Single* v);
	public static void Uniform2 (int location, int x, int y);
	public static void Uniform3 (int location, int count, System.Int32* v);
	public static void Uniform3 (int location, uint v0, uint v1, uint v2);
	public static void Uniform3 (int location, int count, System.UInt32[] value);
	public static void Uniform3 (int location, int count, System.UInt32& value);
	public static void Uniform3 (int location, int count, System.UInt32* value);
	public static void Uniform3 (int location, int count, System.Int32& v);
	public static void Uniform3 (int location, float x, float y, float z);
	public static void Uniform3 (int location, int count, System.Single[] v);
	public static void Uniform3 (int location, int count, System.Single& v);
	public static void Uniform3 (int location, int count, System.Single* v);
	public static void Uniform3 (int location, int x, int y, int z);
	public static void Uniform3 (int location, int count, System.Int32[] v);
	public static void Uniform4 (int location, int count, System.Int32* v);
	public static void Uniform4 (int location, uint v0, uint v1, uint v2, uint v3);
	public static void Uniform4 (int location, int count, System.UInt32[] value);
	public static void Uniform4 (int location, int count, System.UInt32& value);
	public static void Uniform4 (int location, int count, System.UInt32* value);
	public static void Uniform4 (int location, int count, System.Int32& v);
	public static void Uniform4 (int location, float x, float y, float z, float w);
	public static void Uniform4 (int location, int count, System.Single[] v);
	public static void Uniform4 (int location, int count, System.Single& v);
	public static void Uniform4 (int location, int count, System.Int32[] v);
	public static void Uniform4 (int location, int x, int y, int z, int w);
	public static void Uniform4 (int location, int count, System.Single* v);
	public static void UniformBlockBinding (int program, int uniformBlockIndex, int uniformBlockBinding);
	public static void UniformBlockBinding (uint program, uint uniformBlockIndex, uint uniformBlockBinding);
	public static void UniformMatrix2 (int location, int count, bool transpose, System.Single* value);
	public static void UniformMatrix2 (int location, int count, bool transpose, System.Single& value);
	public static void UniformMatrix2 (int location, int count, bool transpose, System.Single[] value);
	public static void UniformMatrix2x3 (int location, int count, bool transpose, System.Single[] value);
	public static void UniformMatrix2x3 (int location, int count, bool transpose, System.Single& value);
	public static void UniformMatrix2x3 (int location, int count, bool transpose, System.Single* value);
	public static void UniformMatrix2x4 (int location, int count, bool transpose, System.Single* value);
	public static void UniformMatrix2x4 (int location, int count, bool transpose, System.Single& value);
	public static void UniformMatrix2x4 (int location, int count, bool transpose, System.Single[] value);
	public static void UniformMatrix3 (int location, int count, bool transpose, System.Single[] value);
	public static void UniformMatrix3 (int location, int count, bool transpose, System.Single& value);
	public static void UniformMatrix3 (int location, int count, bool transpose, System.Single* value);
	public static void UniformMatrix3x2 (int location, int count, bool transpose, System.Single* value);
	public static void UniformMatrix3x2 (int location, int count, bool transpose, System.Single& value);
	public static void UniformMatrix3x2 (int location, int count, bool transpose, System.Single[] value);
	public static void UniformMatrix3x4 (int location, int count, bool transpose, System.Single[] value);
	public static void UniformMatrix3x4 (int location, int count, bool transpose, System.Single& value);
	public static void UniformMatrix3x4 (int location, int count, bool transpose, System.Single* value);
	public static void UniformMatrix4 (int location, int count, bool transpose, System.Single* value);
	public static void UniformMatrix4 (int location, int count, bool transpose, System.Single& value);
	public static void UniformMatrix4 (int location, int count, bool transpose, System.Single[] value);
	public static void UniformMatrix4x2 (int location, int count, bool transpose, System.Single[] value);
	public static void UniformMatrix4x2 (int location, int count, bool transpose, System.Single& value);
	public static void UniformMatrix4x2 (int location, int count, bool transpose, System.Single* value);
	public static void UniformMatrix4x3 (int location, int count, bool transpose, System.Single* value);
	public static void UniformMatrix4x3 (int location, int count, bool transpose, System.Single& value);
	public static void UniformMatrix4x3 (int location, int count, bool transpose, System.Single[] value);
	public static bool UnmapBuffer (All target);
	public static void UseProgram (uint program);
	public static void UseProgram (int program);
	public static void ValidateProgram (int program);
	public static void ValidateProgram (uint program);
	public static void VertexAttrib1 (uint indx, System.Single* values);
	public static void VertexAttrib1 (uint indx, System.Single[] values);
	public static void VertexAttrib1 (int indx, System.Single* values);
	public static void VertexAttrib1 (int indx, float x);
	public static void VertexAttrib1 (uint indx, float x);
	public static void VertexAttrib1 (int indx, System.Single[] values);
	public static void VertexAttrib2 (uint indx, System.Single* values);
	public static void VertexAttrib2 (uint indx, System.Single& values);
	public static void VertexAttrib2 (uint indx, System.Single[] values);
	public static void VertexAttrib2 (int indx, System.Single* values);
	public static void VertexAttrib2 (int indx, float x, float y);
	public static void VertexAttrib2 (uint indx, float x, float y);
	public static void VertexAttrib2 (int indx, System.Single[] values);
	public static void VertexAttrib2 (int indx, System.Single& values);
	public static void VertexAttrib3 (uint indx, System.Single* values);
	public static void VertexAttrib3 (uint indx, System.Single& values);
	public static void VertexAttrib3 (uint indx, System.Single[] values);
	public static void VertexAttrib3 (int indx, System.Single* values);
	public static void VertexAttrib3 (int indx, float x, float y, float z);
	public static void VertexAttrib3 (uint indx, float x, float y, float z);
	public static void VertexAttrib3 (int indx, System.Single[] values);
	public static void VertexAttrib3 (int indx, System.Single& values);
	public static void VertexAttrib4 (uint indx, System.Single* values);
	public static void VertexAttrib4 (uint indx, System.Single& values);
	public static void VertexAttrib4 (uint indx, System.Single[] values);
	public static void VertexAttrib4 (int indx, System.Single* values);
	public static void VertexAttrib4 (int indx, System.Single& values);
	public static void VertexAttrib4 (int indx, System.Single[] values);
	public static void VertexAttrib4 (uint indx, float x, float y, float z, float w);
	public static void VertexAttrib4 (int indx, float x, float y, float z, float w);
	public static void VertexAttribDivisor (uint index, uint divisor);
	public static void VertexAttribDivisor (int index, int divisor);
	public static void VertexAttribI4 (uint index, System.Int32* v);
	public static void VertexAttribI4 (uint index, uint x, uint y, uint z, uint w);
	public static void VertexAttribI4 (uint index, System.UInt32[] v);
	public static void VertexAttribI4 (uint index, System.UInt32& v);
	public static void VertexAttribI4 (uint index, System.UInt32* v);
	public static void VertexAttribI4 (uint index, System.Int32& v);
	public static void VertexAttribI4 (int index, int x, int y, int z, int w);
	public static void VertexAttribI4 (uint index, int x, int y, int z, int w);
	public static void VertexAttribI4 (int index, System.Int32[] v);
	public static void VertexAttribI4 (int index, System.Int32& v);
	public static void VertexAttribI4 (int index, System.Int32* v);
	public static void VertexAttribI4 (uint index, System.Int32[] v);
	public static void VertexAttribIPointer<T4> (uint index, int size, All type, int stride, T4[] pointer);
	public static void VertexAttribIPointer<T4> (uint index, int size, All type, int stride, T4[0...,0...] pointer);
	public static void VertexAttribIPointer<T4> (uint index, int size, All type, int stride, T4[0...,0...,0...] pointer);
	public static void VertexAttribIPointer<T4> (uint index, int size, All type, int stride, T4& pointer);
	public static void VertexAttribIPointer (uint index, int size, All type, int stride, System.IntPtr pointer);
	public static void VertexAttribIPointer (int index, int size, All type, int stride, System.IntPtr pointer);
	public static void VertexAttribIPointer<T4> (int index, int size, All type, int stride, T4[] pointer);
	public static void VertexAttribIPointer<T4> (int index, int size, All type, int stride, T4[0...,0...] pointer);
	public static void VertexAttribIPointer<T4> (int index, int size, All type, int stride, T4[0...,0...,0...] pointer);
	public static void VertexAttribIPointer<T4> (int index, int size, All type, int stride, T4& pointer);
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, T5[] ptr);
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, T5[0...,0...] ptr);
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, T5[0...,0...,0...] ptr);
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, T5& ptr);
	public static void VertexAttribPointer (uint indx, int size, All type, bool normalized, int stride, System.IntPtr ptr);
	public static void VertexAttribPointer (int indx, int size, All type, bool normalized, int stride, System.IntPtr ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, T5[] ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, T5[0...,0...] ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, T5[0...,0...,0...] ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, T5& ptr);
	public static void Viewport (int x, int y, int width, int height);
	public static void WaitSync (System.IntPtr sync, int flags, long timeout);
	public static void WaitSync (System.IntPtr sync, uint flags, ulong timeout);
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
	GenerateMipmapHint = 33170,
}
```

### New Type OpenTK.Graphics.ES30.OpenGlescoreVersions

```
[Serializable]
public enum OpenGlescoreVersions {
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
	Luminance = 6409,
	LuminanceAlpha = 6410,
	Rgb = 6407,
	Rgba = 6408,
}
```

### New Type OpenTK.Graphics.ES30.PixelType

```
[Serializable]
public enum PixelType {
	UnsignedShort4444 = 32819,
	UnsignedShort5551 = 32820,
	UnsignedShort565 = 33635,
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
	ValidateStatus = 35715,
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
}
```

### New Type OpenTK.Graphics.ES30.StringName

```
[Serializable]
public enum StringName {
	Extensions = 7939,
	Renderer = 7937,
	Vendor = 7936,
	Version = 7938,
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
	LinearMipmapLinear = 9987,
	LinearMipmapNearest = 9985,
	NearestMipmapLinear = 9986,
	NearestMipmapNearest = 9984,
}
```

### New Type OpenTK.Graphics.ES30.TextureParameterName

```
[Serializable]
public enum TextureParameterName {
	TextureMagFilter = 10240,
	TextureMinFilter = 10241,
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
	CopyWriteBuffer = 36663,
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

### New Type OpenTK.Graphics.ES30.VertexAttribPointerType

```
[Serializable]
public enum VertexAttribPointerType {
	Byte = 5120,
	Fixed = 5132,
	Float = 5126,
	Short = 5122,
	UnsignedByte = 5121,
	UnsignedShort = 5123,
}
```
