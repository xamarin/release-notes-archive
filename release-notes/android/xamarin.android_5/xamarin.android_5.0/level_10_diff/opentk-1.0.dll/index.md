---
id: D0693DE6-2808-4CC8-856F-BF80E35E76BC
---

## Namespace OpenTK.Graphics

### Type Changed: OpenTK.Graphics.GLVersion

Added value:

```
ES31 = 4,
```

## New Namespace OpenTK.Graphics.ES31

### New Type OpenTK.Graphics.ES31.ActiveAttribType

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

### New Type OpenTK.Graphics.ES31.ActiveUniformBlockParameter

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

### New Type OpenTK.Graphics.ES31.ActiveUniformParameter

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

### New Type OpenTK.Graphics.ES31.ActiveUniformType

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

### New Type OpenTK.Graphics.ES31.All

```
[Serializable]
public enum All {
	ActiveAtomicCounterBuffers = 37593,
	ActiveAttributeMaxLength = 35722,
	ActiveAttributes = 35721,
	ActiveProgram = 33369,
	ActiveResources = 37621,
	ActiveTexture = 34016,
	ActiveUniformBlockMaxNameLength = 35381,
	ActiveUniformBlocks = 35382,
	ActiveUniformMaxLength = 35719,
	ActiveUniforms = 35718,
	ActiveVariables = 37637,
	AliasedLineWidthRange = 33902,
	AliasedPointSizeRange = 33901,
	AllBarrierBits = -1,
	AllShaderBits = -1,
	Alpha = 6406,
	AlphaBits = 3413,
	AlreadySignaled = 37146,
	Always = 519,
	AnySamplesPassed = 35887,
	AnySamplesPassedConservative = 36202,
	ArrayBuffer = 34962,
	ArrayBufferBinding = 34964,
	ArraySize = 37627,
	ArrayStride = 37630,
	AtomicCounterBarrierBit = 4096,
	AtomicCounterBuffer = 37568,
	AtomicCounterBufferBinding = 37569,
	AtomicCounterBufferIndex = 37633,
	AtomicCounterBufferSize = 37571,
	AtomicCounterBufferStart = 37570,
	AttachedShaders = 35717,
	Back = 1029,
	Blend = 3042,
	BlendColor = 32773,
	BlendDstAlpha = 32970,
	BlendDstRgb = 32968,
	BlendEquation = 32777,
	BlendEquationAlpha = 34877,
	BlendEquationRgb = 32777,
	BlendSrcAlpha = 32971,
	BlendSrcRgb = 32969,
	BlockIndex = 37629,
	Blue = 6405,
	BlueBits = 3412,
	Bool = 35670,
	BoolVec2 = 35671,
	BoolVec3 = 35672,
	BoolVec4 = 35673,
	BufferAccessFlags = 37151,
	BufferBinding = 37634,
	BufferDataSize = 37635,
	BufferMapLength = 37152,
	BufferMapOffset = 37153,
	BufferMapped = 35004,
	BufferMapPointer = 35005,
	BufferSize = 34660,
	BufferUpdateBarrierBit = 512,
	BufferUsage = 34661,
	BufferVariable = 37605,
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
	CommandBarrierBit = 64,
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
	ComputeShader = 37305,
	ComputeShaderBit = 32,
	ComputeWorkGroupSize = 33383,
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
	DepthStencilTextureMode = 37098,
	DepthTest = 2929,
	DepthWritemask = 2930,
	DispatchIndirectBuffer = 37102,
	DispatchIndirectBufferBinding = 37103,
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
	DrawIndirectBuffer = 36671,
	DrawIndirectBufferBinding = 36675,
	DstAlpha = 772,
	DstColor = 774,
	DynamicCopy = 35050,
	DynamicDraw = 35048,
	DynamicRead = 35049,
	ElementArrayBarrierBit = 2,
	ElementArrayBuffer = 34963,
	ElementArrayBufferBinding = 34965,
	Equal = 514,
	EsVersion20 = 1,
	EsVersion30 = 1,
	EsVersion31 = 1,
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
	FragmentShaderBit = 2,
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
	FramebufferBarrierBit = 1024,
	FramebufferBinding = 36006,
	FramebufferComplete = 36053,
	FramebufferDefault = 33304,
	FramebufferDefaultFixedSampleLocations = 37652,
	FramebufferDefaultHeight = 37649,
	FramebufferDefaultSamples = 37651,
	FramebufferDefaultWidth = 37648,
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
	Image2D = 36941,
	Image2DArray = 36947,
	Image3D = 36942,
	ImageBindingAccess = 36670,
	ImageBindingFormat = 36974,
	ImageBindingLayer = 36669,
	ImageBindingLayered = 36668,
	ImageBindingLevel = 36667,
	ImageBindingName = 36666,
	ImageCube = 36944,
	ImageFormatCompatibilityByClass = 37065,
	ImageFormatCompatibilityBySize = 37064,
	ImageFormatCompatibilityType = 37063,
	ImgTextureFormatBgra8888 = 1,
	ImplementationColorReadFormat = 35739,
	ImplementationColorReadType = 35738,
	Incr = 7682,
	IncrWrap = 34055,
	InfoLogLength = 35716,
	Int = 5124,
	Int2101010Rev = 36255,
	InterleavedAttribs = 35980,
	IntImage2D = 36952,
	IntImage2DArray = 36958,
	IntImage3D = 36953,
	IntImageCube = 36955,
	IntSampler2D = 36298,
	IntSampler2DArray = 36303,
	IntSampler2DMultisample = 37129,
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
	IsRowMajor = 37632,
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
	Location = 37646,
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
	MatrixStride = 37631,
	Max = 32776,
	Max3DTextureSize = 32883,
	MaxArrayTextureLayers = 35071,
	MaxAtomicCounterBufferBindings = 37596,
	MaxAtomicCounterBufferSize = 37592,
	MaxColorAttachments = 36063,
	MaxColorTextureSamples = 37134,
	MaxCombinedAtomicCounterBuffers = 37585,
	MaxCombinedAtomicCounters = 37591,
	MaxCombinedComputeUniformComponents = 33382,
	MaxCombinedFragmentUniformComponents = 35379,
	MaxCombinedImageUniforms = 37071,
	MaxCombinedShaderOutputResources = 36665,
	MaxCombinedShaderStorageBlocks = 37084,
	MaxCombinedTextureImageUnits = 35661,
	MaxCombinedUniformBlocks = 35374,
	MaxCombinedVertexUniformComponents = 35377,
	MaxComputeAtomicCounterBuffers = 33380,
	MaxComputeAtomicCounters = 33381,
	MaxComputeImageUniforms = 37309,
	MaxComputeShaderStorageBlocks = 37083,
	MaxComputeSharedMemorySize = 33378,
	MaxComputeTextureImageUnits = 37308,
	MaxComputeUniformBlocks = 37307,
	MaxComputeUniformComponents = 33379,
	MaxComputeWorkGroupCount = 37310,
	MaxComputeWorkGroupInvocations = 37099,
	MaxComputeWorkGroupSize = 37311,
	MaxCubeMapTextureSize = 34076,
	MaxDepthTextureSamples = 37135,
	MaxDrawBuffers = 34852,
	MaxElementIndex = 36203,
	MaxElementsIndices = 33001,
	MaxElementsVertices = 33000,
	MaxFragmentAtomicCounterBuffers = 37584,
	MaxFragmentAtomicCounters = 37590,
	MaxFragmentImageUniforms = 37070,
	MaxFragmentInputComponents = 37157,
	MaxFragmentShaderStorageBlocks = 37082,
	MaxFragmentUniformBlocks = 35373,
	MaxFragmentUniformComponents = 35657,
	MaxFragmentUniformVectors = 36349,
	MaxFramebufferHeight = 37654,
	MaxFramebufferSamples = 37656,
	MaxFramebufferWidth = 37653,
	MaxImageUnits = 36664,
	MaxIntegerSamples = 37136,
	MaxNameLength = 37622,
	MaxNumActiveVariables = 37623,
	MaxProgramTexelOffset = 35077,
	MaxProgramTextureGatherOffset = 36447,
	MaxRenderbufferSize = 34024,
	MaxSampleMaskWords = 36441,
	MaxSamples = 36183,
	MaxServerWaitTimeout = 37137,
	MaxShaderStorageBlockSize = 37086,
	MaxShaderStorageBufferBindings = 37085,
	MaxTextureImageUnits = 34930,
	MaxTextureLodBias = 34045,
	MaxTextureSize = 3379,
	MaxTransformFeedbackInterleavedComponents = 35978,
	MaxTransformFeedbackSeparateAttribs = 35979,
	MaxTransformFeedbackSeparateComponents = 35968,
	MaxUniformBlockSize = 35376,
	MaxUniformBufferBindings = 35375,
	MaxUniformLocations = 33390,
	MaxVaryingComponents = 35659,
	MaxVaryingVectors = 36348,
	MaxVertexAtomicCounterBuffers = 37580,
	MaxVertexAtomicCounters = 37586,
	MaxVertexAttribBindings = 33498,
	MaxVertexAttribRelativeOffset = 33497,
	MaxVertexAttribs = 34921,
	MaxVertexAttribStride = 33509,
	MaxVertexImageUniforms = 37066,
	MaxVertexOutputComponents = 37154,
	MaxVertexShaderStorageBlocks = 37078,
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
	MinProgramTextureGatherOffset = 36446,
	MirroredRepeat = 33648,
	NameLength = 37625,
	Nearest = 9728,
	NearestMipmapLinear = 9986,
	NearestMipmapNearest = 9984,
	Never = 512,
	Nicest = 4354,
	NoError = 0,
	None = 0,
	Notequal = 517,
	NumActiveVariables = 37636,
	NumCompressedTextureFormats = 34466,
	NumExtensions = 33309,
	NumProgramBinaryFormats = 34814,
	NumSampleCounts = 37760,
	NumShaderBinaryFormats = 36345,
	ObjectType = 37138,
	Offset = 37628,
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
	PixelBufferBarrierBit = 128,
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
	ProgramInput = 37603,
	ProgramOutput = 37604,
	ProgramPipelineBinding = 33370,
	ProgramSeparable = 33368,
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
	ReadOnly = 35000,
	ReadWrite = 35002,
	Red = 6403,
	RedBits = 3410,
	RedInteger = 36244,
	ReferencedByComputeShader = 37643,
	ReferencedByFragmentShader = 37642,
	ReferencedByVertexShader = 37638,
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
	SampleMask = 36433,
	SampleMaskValue = 36434,
	SamplePosition = 36432,
	Sampler2D = 35678,
	Sampler2DArray = 36289,
	Sampler2DArrayShadow = 36292,
	Sampler2DMultisample = 37128,
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
	ShaderImageAccessBarrierBit = 32,
	ShaderSourceLength = 35720,
	ShaderStorageBarrierBit = 8192,
	ShaderStorageBlock = 37606,
	ShaderStorageBuffer = 37074,
	ShaderStorageBufferBinding = 37075,
	ShaderStorageBufferOffsetAlignment = 37087,
	ShaderStorageBufferSize = 37077,
	ShaderStorageBufferStart = 37076,
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
	Texture2DMultisample = 37120,
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
	TextureAlphaSize = 32863,
	TextureAlphaType = 35859,
	TextureBaseLevel = 33084,
	TextureBinding2D = 32873,
	TextureBinding2DArray = 35869,
	TextureBinding2DMultisample = 37124,
	TextureBinding3D = 32874,
	TextureBindingCubeMap = 34068,
	TextureBlueSize = 32862,
	TextureBlueType = 35858,
	TextureCompareFunc = 34893,
	TextureCompareMode = 34892,
	TextureCompressed = 34465,
	TextureCubeMap = 34067,
	TextureCubeMapNegativeX = 34070,
	TextureCubeMapNegativeY = 34072,
	TextureCubeMapNegativeZ = 34074,
	TextureCubeMapPositiveX = 34069,
	TextureCubeMapPositiveY = 34071,
	TextureCubeMapPositiveZ = 34073,
	TextureDepth = 32881,
	TextureDepthSize = 34890,
	TextureDepthType = 35862,
	TextureFetchBarrierBit = 8,
	TextureFixedSampleLocations = 37127,
	TextureGreenSize = 32861,
	TextureGreenType = 35857,
	TextureHeight = 4097,
	TextureImmutableFormat = 37167,
	TextureImmutableLevels = 33503,
	TextureInternalFormat = 4099,
	TextureMagFilter = 10240,
	TextureMaxLevel = 33085,
	TextureMaxLod = 33083,
	TextureMinFilter = 10241,
	TextureMinLod = 33082,
	TextureRedSize = 32860,
	TextureRedType = 35856,
	TextureSamples = 37126,
	TextureSharedSize = 35903,
	TextureStencilSize = 35057,
	TextureSwizzleA = 36421,
	TextureSwizzleB = 36420,
	TextureSwizzleG = 36419,
	TextureSwizzleR = 36418,
	TextureUpdateBarrierBit = 256,
	TextureWidth = 4096,
	TextureWrapR = 32882,
	TextureWrapS = 10242,
	TextureWrapT = 10243,
	TimeoutExpired = 37147,
	TimeoutIgnored = -1,
	TopLevelArraySize = 37644,
	TopLevelArrayStride = 37645,
	TransformFeedback = 36386,
	TransformFeedbackActive = 36388,
	TransformFeedbackBarrierBit = 2048,
	TransformFeedbackBinding = 36389,
	TransformFeedbackBuffer = 35982,
	TransformFeedbackBufferBinding = 35983,
	TransformFeedbackBufferMode = 35967,
	TransformFeedbackBufferSize = 35973,
	TransformFeedbackBufferStart = 35972,
	TransformFeedbackPaused = 36387,
	TransformFeedbackPrimitivesWritten = 35976,
	TransformFeedbackVarying = 37620,
	TransformFeedbackVaryingMaxLength = 35958,
	TransformFeedbackVaryings = 35971,
	TriangleFan = 6,
	Triangles = 4,
	TriangleStrip = 5,
	True = 1,
	Type = 37626,
	Uniform = 37601,
	UniformArrayStride = 35388,
	UniformBarrierBit = 4,
	UniformBlock = 37602,
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
	UnsignedIntAtomicCounter = 37595,
	UnsignedIntImage2D = 36963,
	UnsignedIntImage2DArray = 36969,
	UnsignedIntImage3D = 36964,
	UnsignedIntImageCube = 36966,
	UnsignedIntSampler2D = 36306,
	UnsignedIntSampler2DArray = 36311,
	UnsignedIntSampler2DMultisample = 37130,
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
	VertexAttribArrayBarrierBit = 1,
	VertexAttribArrayBufferBinding = 34975,
	VertexAttribArrayDivisor = 35070,
	VertexAttribArrayEnabled = 34338,
	VertexAttribArrayInteger = 35069,
	VertexAttribArrayNormalized = 34922,
	VertexAttribArrayPointer = 34373,
	VertexAttribArraySize = 34339,
	VertexAttribArrayStride = 34340,
	VertexAttribArrayType = 34341,
	VertexAttribBinding = 33492,
	VertexAttribRelativeOffset = 33493,
	VertexBindingBuffer = 36687,
	VertexBindingDivisor = 33494,
	VertexBindingOffset = 33495,
	VertexBindingStride = 33496,
	VertexShader = 35633,
	VertexShaderBit = 1,
	Viewport = 2978,
	WaitFailed = 37149,
	WriteOnly = 35001,
	Zero = 0,
}
```

### New Type OpenTK.Graphics.ES31.BeginMode

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

### New Type OpenTK.Graphics.ES31.BlendEquationMode

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

### New Type OpenTK.Graphics.ES31.BlendEquationSeparate

```
[Serializable]
public enum BlendEquationSeparate {
	BlendEquation = 32777,
	BlendEquationAlpha = 34877,
	FuncAdd = 32774,
}
```

### New Type OpenTK.Graphics.ES31.BlendingFactorDest

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

### New Type OpenTK.Graphics.ES31.BlendingFactorSrc

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

### New Type OpenTK.Graphics.ES31.BlendSubtract

```
[Serializable]
public enum BlendSubtract {
	FuncReverseSubtract = 32779,
	FuncSubtract = 32778,
}
```

### New Type OpenTK.Graphics.ES31.BlitFramebufferFilter

```
[Serializable]
public enum BlitFramebufferFilter {
	Linear = 9729,
	Nearest = 9728,
}
```

### New Type OpenTK.Graphics.ES31.Boolean

```
[Serializable]
public enum Boolean {
	False = 0,
	True = 1,
}
```

### New Type OpenTK.Graphics.ES31.BufferAccessMask

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

### New Type OpenTK.Graphics.ES31.BufferObjects

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

### New Type OpenTK.Graphics.ES31.BufferParameterName

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

### New Type OpenTK.Graphics.ES31.BufferPointer

```
[Serializable]
public enum BufferPointer {
	BufferMapPointer = 35005,
}
```

### New Type OpenTK.Graphics.ES31.BufferRangeTarget

```
[Serializable]
public enum BufferRangeTarget {
	TransformFeedbackBuffer = 35982,
	UniformBuffer = 35345,
}
```

### New Type OpenTK.Graphics.ES31.BufferTarget

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

### New Type OpenTK.Graphics.ES31.BufferUsage

```
[Serializable]
public enum BufferUsage {
	DynamicDraw = 35048,
	StaticDraw = 35044,
	StreamDraw = 35040,
}
```

### New Type OpenTK.Graphics.ES31.ClearBuffer

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

### New Type OpenTK.Graphics.ES31.ClearBufferCombined

```
[Serializable]
public enum ClearBufferCombined {
	DepthStencil = 34041,
}
```

### New Type OpenTK.Graphics.ES31.ClearBufferMask

```
[Serializable]
[Flags]
public enum ClearBufferMask {
	ColorBufferBit = 16384,
	DepthBufferBit = 256,
	StencilBufferBit = 1024,
}
```

### New Type OpenTK.Graphics.ES31.CompressedInternalFormat

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

### New Type OpenTK.Graphics.ES31.CullFaceMode

```
[Serializable]
public enum CullFaceMode {
	Back = 1029,
	Front = 1028,
	FrontAndBack = 1032,
}
```

### New Type OpenTK.Graphics.ES31.DataType

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

### New Type OpenTK.Graphics.ES31.DepthFunction

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

### New Type OpenTK.Graphics.ES31.DrawBufferMode

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

### New Type OpenTK.Graphics.ES31.DrawElementsType

```
[Serializable]
public enum DrawElementsType {
	UnsignedByte = 5121,
	UnsignedInt = 5125,
	UnsignedShort = 5123,
}
```

### New Type OpenTK.Graphics.ES31.EnableCap

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

### New Type OpenTK.Graphics.ES31.ErrorCode

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

### New Type OpenTK.Graphics.ES31.FramebufferAttachment

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

### New Type OpenTK.Graphics.ES31.FramebufferErrorCode

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

### New Type OpenTK.Graphics.ES31.FramebufferObject

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

### New Type OpenTK.Graphics.ES31.FramebufferParameterName

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

### New Type OpenTK.Graphics.ES31.FramebufferSlot

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

### New Type OpenTK.Graphics.ES31.FramebufferTarget

```
[Serializable]
public enum FramebufferTarget {
	DrawFramebuffer = 36009,
	Framebuffer = 36160,
	ReadFramebuffer = 36008,
}
```

### New Type OpenTK.Graphics.ES31.FrontFaceDirection

```
[Serializable]
public enum FrontFaceDirection {
	Ccw = 2305,
	Cw = 2304,
}
```

### New Type OpenTK.Graphics.ES31.GetIndexedPName

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

### New Type OpenTK.Graphics.ES31.GetPName

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

### New Type OpenTK.Graphics.ES31.GetQueryObjectParam

```
[Serializable]
public enum GetQueryObjectParam {
	QueryResult = 34918,
	QueryResultAvailable = 34919,
}
```

### New Type OpenTK.Graphics.ES31.GetQueryParam

```
[Serializable]
public enum GetQueryParam {
	CurrentQuery = 34917,
}
```

### New Type OpenTK.Graphics.ES31.GetTextureParameter

```
[Serializable]
public enum GetTextureParameter {
	CompressedTextureFormats = 34467,
	NumCompressedTextureFormats = 34466,
	TextureAlphaSize = 32863,
	TextureBaseLevel = 33084,
	TextureBlueSize = 32862,
	TextureCompareFunc = 34893,
	TextureCompareMode = 34892,
	TextureGreenSize = 32861,
	TextureHeight = 4097,
	TextureImmutableFormat = 37167,
	TextureInternalFormat = 4099,
	TextureMagFilter = 10240,
	TextureMaxLevel = 33085,
	TextureMaxLod = 33083,
	TextureMinFilter = 10241,
	TextureMinLod = 33082,
	TextureRedSize = 32860,
	TextureSwizzleA = 36421,
	TextureSwizzleB = 36420,
	TextureSwizzleG = 36419,
	TextureSwizzleR = 36418,
	TextureWidth = 4096,
	TextureWrapR = 32882,
	TextureWrapS = 10242,
	TextureWrapT = 10243,
}
```

### New Type OpenTK.Graphics.ES31.GL

```
public sealed class GL : OpenTK.Graphics.GraphicsBindingsBase {
	// constructors
	public GL ();
	// fields
	public static const string Library = "libGLESv2.dll";
	// properties
	protected override object SyncRoot { get; }
	// methods
	public static void ActiveShaderProgram (int pipeline, int program);
	public static void ActiveShaderProgram (uint pipeline, uint program);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ActiveTexture (All texture);
	public static void ActiveTexture (TextureUnit texture);
	public static void AttachShader (int program, int shader);
	public static void AttachShader (uint program, uint shader);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BeginQuery (All target, int id);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BeginQuery (All target, uint id);
	public static void BeginQuery (QueryTarget target, int id);
	public static void BeginQuery (QueryTarget target, uint id);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BeginTransformFeedback (All primitiveMode);
	public static void BeginTransformFeedback (TransformFeedbackPrimitiveType primitiveMode);
	public static void BindAttribLocation (uint program, uint index, string name);
	public static void BindAttribLocation (int program, int index, string name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindBuffer (All target, uint buffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindBuffer (All target, int buffer);
	public static void BindBuffer (BufferTarget target, int buffer);
	public static void BindBuffer (BufferTarget target, uint buffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindBufferBase (All target, int index, int buffer);
	public static void BindBufferBase (BufferRangeTarget target, int index, int buffer);
	public static void BindBufferBase (BufferRangeTarget target, uint index, uint buffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindBufferBase (All target, uint index, uint buffer);
	public static void BindBufferRange (BufferRangeTarget target, int index, int buffer, System.IntPtr offset, System.IntPtr size);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindBufferRange (All target, uint index, uint buffer, System.IntPtr offset, System.IntPtr size);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindBufferRange (All target, int index, int buffer, System.IntPtr offset, System.IntPtr size);
	public static void BindBufferRange (BufferRangeTarget target, uint index, uint buffer, System.IntPtr offset, System.IntPtr size);
	public static void BindFramebuffer (FramebufferTarget target, int framebuffer);
	public static void BindFramebuffer (FramebufferTarget target, uint framebuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindFramebuffer (All target, uint framebuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindFramebuffer (All target, int framebuffer);
	public static void BindImageTexture (int unit, int texture, int level, bool layered, int layer, All access, All format);
	public static void BindImageTexture (uint unit, uint texture, int level, bool layered, int layer, All access, All format);
	public static void BindProgramPipeline (uint pipeline);
	public static void BindProgramPipeline (int pipeline);
	public static void BindRenderbuffer (RenderbufferTarget target, int renderbuffer);
	public static void BindRenderbuffer (RenderbufferTarget target, uint renderbuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindRenderbuffer (All target, uint renderbuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindRenderbuffer (All target, int renderbuffer);
	public static void BindSampler (int unit, int sampler);
	public static void BindSampler (uint unit, uint sampler);
	public static void BindTexture (TextureTarget target, uint texture);
	public static void BindTexture (TextureTarget target, int texture);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindTexture (All target, uint texture);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindTexture (All target, int texture);
	public static void BindTransformFeedback (TransformFeedbackTarget target, int id);
	public static void BindTransformFeedback (TransformFeedbackTarget target, uint id);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindTransformFeedback (All target, int id);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BindTransformFeedback (All target, uint id);
	public static void BindVertexArray (int array);
	public static void BindVertexArray (uint array);
	public static void BindVertexBuffer (uint bindingindex, uint buffer, System.IntPtr offset, int stride);
	public static void BindVertexBuffer (int bindingindex, int buffer, System.IntPtr offset, int stride);
	public static void BlendColor (float red, float green, float blue, float alpha);
	public static void BlendColor (System.Drawing.Color color);
	public static void BlendColor (OpenTK.Graphics.Color4 color);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlendEquation (All mode);
	public static void BlendEquation (BlendEquationMode mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlendEquationSeparate (All modeRGB, All modeAlpha);
	public static void BlendEquationSeparate (BlendEquationMode modeRGB, BlendEquationMode modeAlpha);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlendFunc (All sfactor, All dfactor);
	public static void BlendFunc (BlendingFactorSrc sfactor, BlendingFactorDest dfactor);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlendFuncSeparate (All srcRGB, All dstRGB, All srcAlpha, All dstAlpha);
	public static void BlendFuncSeparate (BlendingFactorSrc srcRGB, BlendingFactorDest dstRGB, BlendingFactorSrc srcAlpha, BlendingFactorDest dstAlpha);
	public static void BlitFramebuffer (int srcX0, int srcY0, int srcX1, int srcY1, int dstX0, int dstY0, int dstX1, int dstY1, ClearBufferMask mask, BlitFramebufferFilter filter);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlitFramebuffer (int srcX0, int srcY0, int srcX1, int srcY1, int dstX0, int dstY0, int dstX1, int dstY1, uint mask, All filter);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void BlitFramebuffer (int srcX0, int srcY0, int srcX1, int srcY1, int dstX0, int dstY0, int dstX1, int dstY1, int mask, All filter);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, out T2 data, BufferUsage usage);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, T2[0...,0...] data, BufferUsage usage);
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, T2[] data, BufferUsage usage);
	public static void BufferData (BufferTarget target, System.IntPtr size, System.IntPtr data, BufferUsage usage);

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
	public static void BufferData<T2> (BufferTarget target, System.IntPtr size, T2[0...,0...,0...] data, BufferUsage usage);

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
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, out T3 data);
	public static void BufferSubData (BufferTarget target, System.IntPtr offset, System.IntPtr size, System.IntPtr data);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, T3[] data);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, T3[0...,0...] data);
	public static void BufferSubData<T3> (BufferTarget target, System.IntPtr offset, System.IntPtr size, T3[0...,0...,0...] data);
	public static FramebufferErrorCode CheckFramebufferStatus (FramebufferTarget target);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static All CheckFramebufferStatus (All target);
	public static void Clear (ClearBufferMask mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, int* value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, float* value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, ref float value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, float[] value);
	public static void ClearBuffer (ClearBufferCombined buffer, int drawbuffer, float depth, int stencil);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, int[] value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, ref int value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, float* value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, int[] value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, ref int value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, uint* value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, ref uint value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, uint[] value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, ref float value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, int* value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, uint[] value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, ref uint value);
	public static void ClearBuffer (ClearBuffer buffer, int drawbuffer, uint* value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, float depth, int stencil);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ClearBuffer (All buffer, int drawbuffer, float[] value);
	public static void ClearColor (float red, float green, float blue, float alpha);
	public static void ClearColor (System.Drawing.Color color);
	public static void ClearColor (OpenTK.Graphics.Color4 color);
	public static void ClearDepth (float depth);
	public static void ClearStencil (int s);
	public static All ClientWaitSync (System.IntPtr sync, int flags, long timeout);
	public static All ClientWaitSync (System.IntPtr sync, uint flags, ulong timeout);
	public static void ColorMask (bool red, bool green, bool blue, bool alpha);
	public static void CompileShader (uint shader);
	public static void CompileShader (int shader);
	public static void CompressedTexImage2D (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, System.IntPtr data);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, T7[0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, T7[0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, out T7 data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, T7[0...,0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D<T7> (All target, int level, All internalformat, int width, int height, int border, int imageSize, T7[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage2D (All target, int level, All internalformat, int width, int height, int border, int imageSize, System.IntPtr data);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, T7[0...,0...,0...] data);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, T7[] data);
	public static void CompressedTexImage2D<T7> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, int imageSize, out T7 data);
	public static void CompressedTexImage3D (TextureTarget3D target, int level, CompressedInternalFormat internalformat, int width, int height, int depth, int border, int imageSize, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage3D<T8> (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, T8[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage3D<T8> (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, T8[0...,0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage3D<T8> (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, out T8 data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage3D (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexImage3D<T8> (All target, int level, All internalformat, int width, int height, int depth, int border, int imageSize, T8[0...,0...] data);
	public static void CompressedTexImage3D<T8> (TextureTarget3D target, int level, CompressedInternalFormat internalformat, int width, int height, int depth, int border, int imageSize, T8[] data);
	public static void CompressedTexImage3D<T8> (TextureTarget3D target, int level, CompressedInternalFormat internalformat, int width, int height, int depth, int border, int imageSize, out T8 data);
	public static void CompressedTexImage3D<T8> (TextureTarget3D target, int level, CompressedInternalFormat internalformat, int width, int height, int depth, int border, int imageSize, T8[0...,0...,0...] data);
	public static void CompressedTexImage3D<T8> (TextureTarget3D target, int level, CompressedInternalFormat internalformat, int width, int height, int depth, int border, int imageSize, T8[0...,0...] data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, T8[0...,0...] data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, out T8 data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, T8[0...,0...,0...] data);
	public static void CompressedTexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, T8[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, T8[0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, T8[0...,0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, out T8 data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, int imageSize, T8[] data);
	public static void CompressedTexSubImage2D (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, int imageSize, System.IntPtr data);
	public static void CompressedTexSubImage3D (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, CompressedInternalFormat format, int imageSize, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, T10[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage3D (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, System.IntPtr data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, T10[0...,0...,0...] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, out T10 data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CompressedTexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, int imageSize, T10[0...,0...] data);
	public static void CompressedTexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, CompressedInternalFormat format, int imageSize, T10[] data);
	public static void CompressedTexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, CompressedInternalFormat format, int imageSize, T10[0...,0...] data);
	public static void CompressedTexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, CompressedInternalFormat format, int imageSize, out T10 data);
	public static void CompressedTexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, CompressedInternalFormat format, int imageSize, T10[0...,0...,0...] data);
	public static void CopyBufferSubData (BufferTarget readTarget, BufferTarget writeTarget, System.IntPtr readOffset, System.IntPtr writeOffset, System.IntPtr size);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CopyBufferSubData (All readTarget, All writeTarget, System.IntPtr readOffset, System.IntPtr writeOffset, System.IntPtr size);
	public static void CopyTexImage2D (TextureTarget target, int level, PixelInternalFormat internalformat, int x, int y, int width, int height, int border);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CopyTexImage2D (All target, int level, All internalformat, int x, int y, int width, int height, int border);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CopyTexSubImage2D (All target, int level, int xoffset, int yoffset, int x, int y, int width, int height);
	public static void CopyTexSubImage2D (TextureTarget target, int level, int xoffset, int yoffset, int x, int y, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CopyTexSubImage3D (All target, int level, int xoffset, int yoffset, int zoffset, int x, int y, int width, int height);
	public static void CopyTexSubImage3D (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int x, int y, int width, int height);
	public static int CreateProgram ();
	public static int CreateShader (ShaderType type);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int CreateShader (All type);
	public static int CreateShaderProgram (All type, int count, string const);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void CullFace (All mode);
	public static void CullFace (CullFaceMode mode);
	public static void DeleteBuffers (int n, int[] buffers);
	public static void DeleteBuffers (int n, ref int buffers);
	public static void DeleteBuffers (int n, int* buffers);
	public static void DeleteBuffers (int n, uint[] buffers);
	public static void DeleteBuffers (int n, ref uint buffers);
	public static void DeleteBuffers (int n, uint* buffers);
	public static void DeleteFramebuffers (int n, ref uint framebuffers);
	public static void DeleteFramebuffers (int n, int* framebuffers);
	public static void DeleteFramebuffers (int n, ref int framebuffers);
	public static void DeleteFramebuffers (int n, int[] framebuffers);
	public static void DeleteFramebuffers (int n, uint* framebuffers);
	public static void DeleteFramebuffers (int n, uint[] framebuffers);
	public static void DeleteProgram (int program);
	public static void DeleteProgram (uint program);
	public static void DeleteProgramPipelines (int n, int[] pipelines);
	public static void DeleteProgramPipelines (int n, uint* pipelines);
	public static void DeleteProgramPipelines (int n, ref uint pipelines);
	public static void DeleteProgramPipelines (int n, ref int pipelines);
	public static void DeleteProgramPipelines (int n, int* pipelines);
	public static void DeleteProgramPipelines (int n, uint[] pipelines);
	public static void DeleteQueries (int n, uint[] ids);
	public static void DeleteQueries (int n, int* ids);
	public static void DeleteQueries (int n, ref int ids);
	public static void DeleteQueries (int n, int[] ids);
	public static void DeleteQueries (int n, ref uint ids);
	public static void DeleteQueries (int n, uint* ids);
	public static void DeleteRenderbuffers (int n, int[] renderbuffers);
	public static void DeleteRenderbuffers (int n, int* renderbuffers);
	public static void DeleteRenderbuffers (int n, uint[] renderbuffers);
	public static void DeleteRenderbuffers (int n, ref uint renderbuffers);
	public static void DeleteRenderbuffers (int n, uint* renderbuffers);
	public static void DeleteRenderbuffers (int n, ref int renderbuffers);
	public static void DeleteSamplers (int count, uint[] samplers);
	public static void DeleteSamplers (int count, uint* samplers);
	public static void DeleteSamplers (int count, ref uint samplers);
	public static void DeleteSamplers (int count, int[] samplers);
	public static void DeleteSamplers (int count, int* samplers);
	public static void DeleteSamplers (int count, ref int samplers);
	public static void DeleteShader (uint shader);
	public static void DeleteShader (int shader);
	public static void DeleteSync (System.IntPtr sync);
	public static void DeleteTexture (uint id);
	public static void DeleteTexture (int id);
	public static void DeleteTextures (int n, uint* textures);
	public static void DeleteTextures (int n, ref uint textures);
	public static void DeleteTextures (int n, uint[] textures);
	public static void DeleteTextures (int n, int* textures);
	public static void DeleteTextures (int n, ref int textures);
	public static void DeleteTextures (int n, int[] textures);
	public static void DeleteTransformFeedback (int n, uint* ids);
	public static void DeleteTransformFeedback (int n, ref uint ids);
	public static void DeleteTransformFeedback (int n, uint[] ids);
	public static void DeleteTransformFeedback (int n, int[] ids);
	public static void DeleteTransformFeedback (int n, ref int ids);
	public static void DeleteTransformFeedback (int n, int* ids);
	public static void DeleteVertexArrays (int n, uint* arrays);
	public static void DeleteVertexArrays (int n, ref uint arrays);
	public static void DeleteVertexArrays (int n, uint[] arrays);
	public static void DeleteVertexArrays (int n, int* arrays);
	public static void DeleteVertexArrays (int n, ref int arrays);
	public static void DeleteVertexArrays (int n, int[] arrays);
	public static void DepthFunc (DepthFunction func);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DepthFunc (All func);
	public static void DepthMask (bool flag);
	public static void DepthRange (float n, float f);
	public static void DetachShader (uint program, uint shader);
	public static void DetachShader (int program, int shader);
	public static void Disable (EnableCap cap);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void Disable (All cap);
	public static void DisableVertexAttribArray (int index);
	public static void DisableVertexAttribArray (uint index);
	public static void DispatchCompute (uint num_groups_x, uint num_groups_y, uint num_groups_z);
	public static void DispatchCompute (int num_groups_x, int num_groups_y, int num_groups_z);
	public static void DispatchComputeIndirect (System.IntPtr indirect);
	public static void DrawArrays (BeginMode mode, int first, int count);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawArrays (All mode, int first, int count);
	public static void DrawArraysIndirect<T1> (PrimitiveType mode, T1[0...,0...,0...] indirect);
	public static void DrawArraysIndirect (PrimitiveType mode, System.IntPtr indirect);
	public static void DrawArraysIndirect<T1> (PrimitiveType mode, T1[0...,0...] indirect);
	public static void DrawArraysIndirect<T1> (PrimitiveType mode, T1[] indirect);
	public static void DrawArraysIndirect<T1> (PrimitiveType mode, out T1 indirect);

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

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements<T3> (All mode, int count, All type, T3[] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements<T3> (All mode, int count, All type, out T3 indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements<T3> (All mode, int count, All type, T3[0...,0...,0...] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements<T3> (All mode, int count, All type, T3[0...,0...] indices);
	public static void DrawElements (BeginMode mode, int count, DrawElementsType type, int offset);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElements (All mode, int count, All type, System.IntPtr indices);
	public static void DrawElements (BeginMode mode, int count, DrawElementsType type, System.IntPtr indices);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, T3[] indices);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, T3[0...,0...] indices);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, T3[0...,0...,0...] indices);
	public static void DrawElements<T3> (BeginMode mode, int count, DrawElementsType type, out T3 indices);
	public static void DrawElementsIndirect (PrimitiveType mode, All type, System.IntPtr indirect);
	public static void DrawElementsIndirect<T2> (PrimitiveType mode, All type, T2[] indirect);
	public static void DrawElementsIndirect<T2> (PrimitiveType mode, All type, T2[0...,0...] indirect);
	public static void DrawElementsIndirect<T2> (PrimitiveType mode, All type, T2[0...,0...,0...] indirect);
	public static void DrawElementsIndirect<T2> (PrimitiveType mode, All type, out T2 indirect);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, out T3 indices, int instanceCount);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElementsInstanced (All mode, int count, All type, System.IntPtr indices, int instanceCount);
	public static void DrawElementsInstanced (PrimitiveType mode, int count, DrawElementsType type, System.IntPtr indices, int instanceCount);
	public static void DrawElementsInstanced<T3> (PrimitiveType mode, int count, DrawElementsType type, T3[] indices, int instanceCount);
	public static void DrawElementsInstanced<T3> (PrimitiveType mode, int count, DrawElementsType type, T3[0...,0...] indices, int instanceCount);
	public static void DrawElementsInstanced<T3> (PrimitiveType mode, int count, DrawElementsType type, T3[0...,0...,0...] indices, int instanceCount);
	public static void DrawElementsInstanced<T3> (PrimitiveType mode, int count, DrawElementsType type, out T3 indices, int instanceCount);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, T3[] indices, int instanceCount);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, T3[0...,0...,0...] indices, int instanceCount);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawElementsInstanced<T3> (All mode, int count, All type, T3[0...,0...] indices, int instanceCount);
	public static void DrawRangeElements (PrimitiveType mode, int start, int end, int count, DrawElementsType type, System.IntPtr indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, int start, int end, int count, DrawElementsType type, T5[] indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, int start, int end, int count, DrawElementsType type, T5[0...,0...] indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, int start, int end, int count, DrawElementsType type, T5[0...,0...,0...] indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, int start, int end, int count, DrawElementsType type, out T5 indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements<T5> (All mode, int start, int end, int count, All type, out T5 indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, uint start, uint end, int count, DrawElementsType type, T5[] indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, uint start, uint end, int count, DrawElementsType type, T5[0...,0...] indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, uint start, uint end, int count, DrawElementsType type, T5[0...,0...,0...] indices);
	public static void DrawRangeElements<T5> (PrimitiveType mode, uint start, uint end, int count, DrawElementsType type, out T5 indices);
	public static void DrawRangeElements (PrimitiveType mode, uint start, uint end, int count, DrawElementsType type, System.IntPtr indices);

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

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements<T5> (All mode, int start, int end, int count, All type, T5[0...,0...] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements<T5> (All mode, int start, int end, int count, All type, T5[] indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements (All mode, int start, int end, int count, All type, System.IntPtr indices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void DrawRangeElements (All mode, uint start, uint end, int count, All type, System.IntPtr indices);
	public static void Enable (EnableCap cap);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void Enable (All cap);
	public static void EnableVertexAttribArray (int index);
	public static void EnableVertexAttribArray (uint index);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void EndQuery (All target);
	public static void EndQuery (QueryTarget target);
	public static void EndTransformFeedback ();
	public static System.IntPtr FenceSync (SyncCondition condition, WaitSyncFlags flags);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static System.IntPtr FenceSync (All condition, int flags);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static System.IntPtr FenceSync (All condition, uint flags);
	public static void Finish ();
	public static void Flush ();

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FlushMappedBufferRange (All target, System.IntPtr offset, System.IntPtr length);
	public static void FlushMappedBufferRange (BufferTarget target, System.IntPtr offset, System.IntPtr length);
	public static void FramebufferParameter (All target, All pname, int param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferRenderbuffer (All target, All attachment, All renderbuffertarget, int renderbuffer);
	public static void FramebufferRenderbuffer (FramebufferTarget target, FramebufferSlot attachment, RenderbufferTarget renderbuffertarget, uint renderbuffer);
	public static void FramebufferRenderbuffer (FramebufferTarget target, FramebufferSlot attachment, RenderbufferTarget renderbuffertarget, int renderbuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferRenderbuffer (All target, All attachment, All renderbuffertarget, uint renderbuffer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferTexture2D (All target, All attachment, All textarget, int texture, int level);
	public static void FramebufferTexture2D (FramebufferTarget target, FramebufferSlot attachment, TextureTarget textarget, uint texture, int level);
	public static void FramebufferTexture2D (FramebufferTarget target, FramebufferSlot attachment, TextureTarget textarget, int texture, int level);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferTexture2D (All target, All attachment, All textarget, uint texture, int level);
	public static void FramebufferTextureLayer (FramebufferTarget target, FramebufferAttachment attachment, int texture, int level, int layer);
	public static void FramebufferTextureLayer (FramebufferTarget target, FramebufferAttachment attachment, uint texture, int level, int layer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferTextureLayer (All target, All attachment, uint texture, int level, int layer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FramebufferTextureLayer (All target, All attachment, int texture, int level, int layer);
	public static void FrontFace (FrontFaceDirection mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void FrontFace (All mode);
	public static void GenBuffers (int n, uint* buffers);
	public static void GenBuffers (int n, out int buffers);
	public static void GenBuffers (int n, int* buffers);
	public static void GenBuffers (int n, uint[] buffers);
	public static void GenBuffers (int n, out uint buffers);
	public static void GenBuffers (int n, int[] buffers);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GenerateMipmap (All target);
	public static void GenerateMipmap (TextureTarget target);
	public static void GenFramebuffers (int n, int[] framebuffers);
	public static void GenFramebuffers (int n, out int framebuffers);
	public static void GenFramebuffers (int n, int* framebuffers);
	public static void GenFramebuffers (int n, uint[] framebuffers);
	public static void GenFramebuffers (int n, out uint framebuffers);
	public static void GenFramebuffers (int n, uint* framebuffers);
	public static void GenProgramPipelines (int n, uint* pipelines);
	public static void GenProgramPipelines (int n, int[] pipelines);
	public static void GenProgramPipelines (int n, out int pipelines);
	public static void GenProgramPipelines (int n, int* pipelines);
	public static void GenProgramPipelines (int n, uint[] pipelines);
	public static void GenProgramPipelines (int n, out uint pipelines);
	public static void GenQueries (int n, int[] ids);
	public static void GenQueries (int n, uint* ids);
	public static void GenQueries (int n, out uint ids);
	public static void GenQueries (int n, uint[] ids);
	public static void GenQueries (int n, int* ids);
	public static void GenQueries (int n, out int ids);
	public static void GenRenderbuffers (int n, uint* renderbuffers);
	public static void GenRenderbuffers (int n, int[] renderbuffers);
	public static void GenRenderbuffers (int n, out int renderbuffers);
	public static void GenRenderbuffers (int n, int* renderbuffers);
	public static void GenRenderbuffers (int n, uint[] renderbuffers);
	public static void GenRenderbuffers (int n, out uint renderbuffers);
	public static void GenSamplers (int count, out int samplers);
	public static void GenSamplers (int count, int* samplers);
	public static void GenSamplers (int count, uint[] samplers);
	public static void GenSamplers (int count, int[] samplers);
	public static void GenSamplers (int count, uint* samplers);
	public static void GenSamplers (int count, out uint samplers);
	public static int GenTexture ();
	public static void GenTextures (int n, uint* textures);
	public static void GenTextures (int n, uint[] textures);
	public static void GenTextures (int n, int* textures);
	public static void GenTextures (int n, out int textures);
	public static void GenTextures (int n, int[] textures);
	public static void GenTextures (int n, out uint textures);
	public static void GenTransformFeedback (int n, int[] ids);
	public static void GenTransformFeedback (int n, int* ids);
	public static void GenTransformFeedback (int n, out int ids);
	public static void GenTransformFeedback (int n, uint[] ids);
	public static void GenTransformFeedback (int n, uint* ids);
	public static void GenTransformFeedback (int n, out uint ids);
	public static void GenVertexArrays (int n, int[] arrays);
	public static void GenVertexArrays (int n, out uint arrays);
	public static void GenVertexArrays (int n, uint* arrays);
	public static void GenVertexArrays (int n, uint[] arrays);
	public static void GenVertexArrays (int n, out int arrays);
	public static void GenVertexArrays (int n, int* arrays);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, out int length, out int size, out ActiveAttribType type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, int[] length, int[] size, ActiveAttribType[] type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (int program, int index, int bufsize, int* length, int* size, ActiveAttribType* type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (int program, int index, int bufsize, out int length, out int size, out ActiveAttribType type, System.Text.StringBuilder name);
	public static void GetActiveAttrib (int program, int index, int bufsize, int[] length, int[] size, ActiveAttribType[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (int program, int index, int bufsize, int[] length, int[] size, All[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (int program, int index, int bufsize, out int length, out int size, out All type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (int program, int index, int bufsize, int* length, int* size, All* type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (uint program, uint index, int bufsize, int[] length, int[] size, All[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (uint program, uint index, int bufsize, out int length, out int size, out All type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveAttrib (uint program, uint index, int bufsize, int* length, int* size, All* type, System.Text.StringBuilder name);
	public static string GetActiveAttrib (int program, int index, out int size, out ActiveAttribType type);

	[Obsolete]
	public static string GetActiveAttrib (int program, int index, out int size, out All type);
	public static void GetActiveAttrib (uint program, uint index, int bufsize, int* length, int* size, ActiveAttribType* type, System.Text.StringBuilder name);
	public static void GetActiveUniform (uint program, uint index, int bufsize, out int length, out int size, out ActiveUniformType type, System.Text.StringBuilder name);
	public static void GetActiveUniform (uint program, uint index, int bufsize, int* length, int* size, ActiveUniformType* type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static string GetActiveUniform (int program, int uniformIndex, out int size, out All type);
	public static void GetActiveUniform (uint program, uint index, int bufsize, int[] length, int[] size, ActiveUniformType[] type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, int* length, int* size, ActiveUniformType* type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, out int length, out int size, out ActiveUniformType type, System.Text.StringBuilder name);
	public static void GetActiveUniform (int program, int index, int bufsize, int[] length, int[] size, ActiveUniformType[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniform (uint program, uint index, int bufsize, int* length, int* size, All* type, System.Text.StringBuilder name);
	public static string GetActiveUniform (int program, int uniformIndex, out int size, out ActiveUniformType type);

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
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, ActiveUniformBlockParameter pname, out int params);
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, ActiveUniformBlockParameter pname, int* params);
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, ActiveUniformBlockParameter pname, int[] params);
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, ActiveUniformBlockParameter pname, out int params);
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, ActiveUniformBlockParameter pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniformBlock (uint program, uint uniformBlockIndex, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, All pname, int[] params);
	public static void GetActiveUniformBlock (int program, int uniformBlockIndex, ActiveUniformBlockParameter pname, int[] params);
	public static void GetActiveUniformBlockName (uint program, uint uniformBlockIndex, int bufSize, out int length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (uint program, uint uniformBlockIndex, int bufSize, int[] length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (int program, int uniformBlockIndex, int bufSize, int* length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (int program, int uniformBlockIndex, int bufSize, out int length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (int program, int uniformBlockIndex, int bufSize, int[] length, System.Text.StringBuilder uniformBlockName);
	public static void GetActiveUniformBlockName (uint program, uint uniformBlockIndex, int bufSize, int* length, System.Text.StringBuilder uniformBlockName);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniforms (int program, int uniformCount, int* uniformIndices, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniforms (int program, int uniformCount, out int uniformIndices, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniforms (int program, int uniformCount, int[] uniformIndices, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniforms (uint program, int uniformCount, uint[] uniformIndices, All pname, int[] params);
	public static void GetActiveUniforms (uint program, int uniformCount, out uint uniformIndices, ActiveUniformParameter pname, out int params);
	public static void GetActiveUniforms (uint program, int uniformCount, uint[] uniformIndices, ActiveUniformParameter pname, int[] params);
	public static void GetActiveUniforms (int program, int uniformCount, int* uniformIndices, ActiveUniformParameter pname, int* params);
	public static void GetActiveUniforms (int program, int uniformCount, out int uniformIndices, ActiveUniformParameter pname, out int params);
	public static void GetActiveUniforms (int program, int uniformCount, int[] uniformIndices, ActiveUniformParameter pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniforms (uint program, int uniformCount, uint* uniformIndices, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetActiveUniforms (uint program, int uniformCount, out uint uniformIndices, All pname, out int params);
	public static void GetActiveUniforms (uint program, int uniformCount, uint* uniformIndices, ActiveUniformParameter pname, int* params);
	public static void GetAttachedShaders (int program, int maxcount, int[] count, int[] shaders);
	public static void GetAttachedShaders (int program, int maxcount, out int count, out int shaders);
	public static void GetAttachedShaders (int program, int maxcount, int* count, int* shaders);
	public static void GetAttachedShaders (uint program, int maxcount, int[] count, uint[] shaders);
	public static void GetAttachedShaders (uint program, int maxcount, out int count, out uint shaders);
	public static void GetAttachedShaders (uint program, int maxcount, int* count, uint* shaders);
	public static int GetAttribLocation (int program, string name);
	public static int GetAttribLocation (uint program, string name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int GetAttribLocation (int program, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int GetAttribLocation (uint program, System.Text.StringBuilder name);
	public static void GetBoolean (GetPName pname, bool* params);
	public static void GetBoolean (All target, int index, bool[] data);
	public static void GetBoolean (All target, int index, out bool data);
	public static void GetBoolean (All target, int index, bool* data);
	public static void GetBoolean (All target, uint index, bool[] data);
	public static void GetBoolean (All target, uint index, out bool data);
	public static void GetBoolean (GetPName pname, bool[] params);
	public static void GetBoolean (GetPName pname, out bool params);
	public static void GetBoolean (All target, uint index, bool* data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBoolean (All pname, bool[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBoolean (All pname, out bool params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBoolean (All pname, bool* params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, long* params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, int[] params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, out int params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, long* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, out long params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, long[] params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, out long params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameter (All target, All pname, int[] params);
	public static void GetBufferParameter (BufferTarget target, BufferParameterName pname, long[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameteri64 (All target, All pname, long[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameteri64 (All target, All pname, long* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferParameteri64 (All target, All pname, out long params);
	public static void GetBufferPointer (BufferTarget target, BufferPointer pname, System.IntPtr params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferPointer (All target, All pname, System.IntPtr params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferPointer<T2> (All target, All pname, T2[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferPointer<T2> (All target, All pname, T2[0...,0...] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferPointer<T2> (All target, All pname, T2[0...,0...,0...] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetBufferPointer<T2> (All target, All pname, out T2 params);
	public static void GetBufferPointer<T2> (BufferTarget target, BufferPointer pname, T2[] params);
	public static void GetBufferPointer<T2> (BufferTarget target, BufferPointer pname, out T2 params);
	public static void GetBufferPointer<T2> (BufferTarget target, BufferPointer pname, T2[0...,0...] params);
	public static void GetBufferPointer<T2> (BufferTarget target, BufferPointer pname, T2[0...,0...,0...] params);

	[Obsolete ("Use the GetErrorCode method, for compatability with Xamarin Android's OpenTK-1.0")]
	public static All GetError ();
	public static ErrorCode GetErrorCode ();
	public static void GetFloat (GetPName pname, out OpenTK.Vector3 vector);
	public static void GetFloat (GetPName pname, float* params);
	public static void GetFloat (GetPName pname, out float params);
	public static void GetFloat (GetPName pname, float[] params);
	public static void GetFloat (GetPName pname, out OpenTK.Vector2 vector);
	public static void GetFloat (GetPName pname, out OpenTK.Vector4 vector);
	public static void GetFloat (GetPName pname, out OpenTK.Matrix4 matrix);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFloat (All pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFloat (All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFloat (All pname, float* params);
	public static int GetFragDataLocation (int program, System.Text.StringBuilder name);
	public static int GetFragDataLocation (uint program, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFramebufferAttachmentParameter (All target, All attachment, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFramebufferAttachmentParameter (All target, All attachment, All pname, int[] params);
	public static void GetFramebufferAttachmentParameter (FramebufferTarget target, FramebufferSlot attachment, FramebufferParameterName pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetFramebufferAttachmentParameter (All target, All attachment, All pname, int* params);
	public static void GetFramebufferAttachmentParameter (FramebufferTarget target, FramebufferSlot attachment, FramebufferParameterName pname, int[] params);
	public static void GetFramebufferAttachmentParameter (FramebufferTarget target, FramebufferSlot attachment, FramebufferParameterName pname, out int params);
	public static void GetFramebufferParameter (All target, All pname, int[] params);
	public static void GetFramebufferParameter (All target, All pname, int* params);
	public static void GetFramebufferParameter (All target, All pname, out int params);
	public static void GetInteger (GetIndexedPName target, int index, int* data);
	public static void GetInteger (GetIndexedPName target, uint index, long* data);
	public static void GetInteger (GetIndexedPName target, int index, out int data);
	public static void GetInteger (GetIndexedPName target, int index, int[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All pname, int[] params);
	public static void GetInteger (GetIndexedPName target, uint index, int[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All pname, out int params);
	public static void GetInteger (GetPName pname, int* params);
	public static void GetInteger (GetPName pname, out int params);
	public static void GetInteger (GetIndexedPName target, uint index, long[] data);
	public static void GetInteger (GetPName pname, int[] params);
	public static void GetInteger (GetIndexedPName target, uint index, int* data);
	public static void GetInteger (GetIndexedPName target, uint index, out int data);
	public static void GetInteger (GetIndexedPName target, uint index, out long data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, uint index, long* data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, int index, int[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, int index, out int data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, int index, int* data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, uint index, int[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, uint index, out int data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, uint index, int* data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, uint index, out long data);
	public static void GetInteger (GetIndexedPName target, int index, long* data);
	public static void GetInteger (GetIndexedPName target, int index, out long data);
	public static void GetInteger (GetIndexedPName target, int index, long[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, int index, long[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, uint index, long[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, int index, long* data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger (All target, int index, out long data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All target, int index, long[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All target, int index, long* data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All target, uint index, long[] data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All target, uint index, out long data);
	public static void GetInteger64 (GetPName pname, out long params);
	public static void GetInteger64 (GetPName pname, long[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All target, int index, out long data);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All pname, long[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All pname, out long params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All pname, long* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInteger64 (All target, uint index, long* data);
	public static void GetInteger64 (GetPName pname, long* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInternalformat (All target, All internalformat, All pname, int bufSize, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInternalformat (All target, All internalformat, All pname, int bufSize, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetInternalformat (All target, All internalformat, All pname, int bufSize, int[] params);
	public static void GetInternalformat (ImageTarget target, SizedInternalFormat internalformat, InternalFormatParameter pname, int bufSize, int* params);
	public static void GetInternalformat (ImageTarget target, SizedInternalFormat internalformat, InternalFormatParameter pname, int bufSize, out int params);
	public static void GetInternalformat (ImageTarget target, SizedInternalFormat internalformat, InternalFormatParameter pname, int bufSize, int[] params);
	public static void GetMultisample (All pname, uint index, float[] val);
	public static void GetMultisample (All pname, uint index, out float val);
	public static void GetMultisample (All pname, int index, float* val);
	public static void GetMultisample (All pname, int index, out float val);
	public static void GetMultisample (All pname, int index, float[] val);
	public static void GetMultisample (All pname, uint index, float* val);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (int program, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (uint program, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (int program, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (int program, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (uint program, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetProgram (uint program, All pname, int* params);
	public static void GetProgram (uint program, ProgramParameter pname, int* params);
	public static void GetProgram (int program, ProgramParameter pname, int[] params);
	public static void GetProgram (int program, ProgramParameter pname, out int params);
	public static void GetProgram (int program, ProgramParameter pname, int* params);
	public static void GetProgram (uint program, ProgramParameter pname, int[] params);
	public static void GetProgram (uint program, ProgramParameter pname, out int params);
	public static void GetProgramBinary<T4> (uint program, int bufSize, out int length, out All binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, out int length, out All binaryFormat, T4[] binary);
	public static void GetProgramBinary (uint program, int bufSize, out int length, out All binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int[] length, All[] binaryFormat, out T4 binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int[] length, All[] binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int[] length, All[] binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, out int length, out All binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int* length, All* binaryFormat, out T4 binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int* length, All* binaryFormat, T4[] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int* length, All* binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int* length, All* binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary (uint program, int bufSize, int* length, All* binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, out int length, out All binaryFormat, out T4 binary);
	public static void GetProgramBinary<T4> (uint program, int bufSize, int[] length, All[] binaryFormat, T4[] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, out int length, out All binaryFormat, T4[] binary);
	public static void GetProgramBinary (int program, int bufSize, out int length, out All binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int[] length, All[] binaryFormat, out T4 binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int[] length, All[] binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int[] length, All[] binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int[] length, All[] binaryFormat, T4[] binary);
	public static void GetProgramBinary (int program, int bufSize, int[] length, All[] binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, out int length, out All binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary (uint program, int bufSize, int[] length, All[] binaryFormat, System.IntPtr binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int* length, All* binaryFormat, out T4 binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int* length, All* binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int* length, All* binaryFormat, T4[0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, int* length, All* binaryFormat, T4[] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, out int length, out All binaryFormat, T4[0...,0...,0...] binary);
	public static void GetProgramBinary<T4> (int program, int bufSize, out int length, out All binaryFormat, out T4 binary);
	public static void GetProgramBinary (int program, int bufSize, int* length, All* binaryFormat, System.IntPtr binary);
	public static void GetProgramInfoLog (uint program, int bufsize, int* length, System.Text.StringBuilder infolog);
	public static void GetProgramInfoLog (uint program, int bufsize, out int length, System.Text.StringBuilder infolog);
	public static void GetProgramInfoLog (uint program, int bufsize, int[] length, System.Text.StringBuilder infolog);
	public static void GetProgramInfoLog (int program, int bufsize, int* length, System.Text.StringBuilder infolog);
	public static string GetProgramInfoLog (int program);
	public static void GetProgramInfoLog (int program, out string info);
	public static void GetProgramInfoLog (int program, int bufsize, int[] length, System.Text.StringBuilder infolog);
	public static void GetProgramInfoLog (int program, int bufsize, out int length, System.Text.StringBuilder infolog);
	public static void GetProgramInterface (int program, All programInterface, All pname, int[] params);
	public static void GetProgramInterface (int program, All programInterface, All pname, out int params);
	public static void GetProgramInterface (uint program, All programInterface, All pname, int* params);
	public static void GetProgramInterface (uint program, All programInterface, All pname, out int params);
	public static void GetProgramInterface (uint program, All programInterface, All pname, int[] params);
	public static void GetProgramInterface (int program, All programInterface, All pname, int* params);
	public static void GetProgramPipeline (uint pipeline, All pname, out int params);
	public static void GetProgramPipeline (uint pipeline, All pname, int* params);
	public static void GetProgramPipeline (int pipeline, All pname, int[] params);
	public static void GetProgramPipeline (int pipeline, All pname, out int params);
	public static void GetProgramPipeline (int pipeline, All pname, int* params);
	public static void GetProgramPipeline (uint pipeline, All pname, int[] params);
	public static void GetProgramPipelineInfoLog (uint pipeline, int bufSize, int[] length, System.Text.StringBuilder infoLog);
	public static void GetProgramPipelineInfoLog (int pipeline, int bufSize, int* length, System.Text.StringBuilder infoLog);
	public static void GetProgramPipelineInfoLog (int pipeline, int bufSize, out int length, System.Text.StringBuilder infoLog);
	public static void GetProgramPipelineInfoLog (int pipeline, int bufSize, int[] length, System.Text.StringBuilder infoLog);
	public static void GetProgramPipelineInfoLog (uint pipeline, int bufSize, int* length, System.Text.StringBuilder infoLog);
	public static void GetProgramPipelineInfoLog (uint pipeline, int bufSize, out int length, System.Text.StringBuilder infoLog);
	public static void GetProgramResource (int program, All programInterface, int index, int propCount, All* props, int bufSize, int* length, int* params);
	public static void GetProgramResource (int program, All programInterface, int index, int propCount, out All props, int bufSize, out int length, out int params);
	public static void GetProgramResource (int program, All programInterface, int index, int propCount, All[] props, int bufSize, int[] length, int[] params);
	public static void GetProgramResource (uint program, All programInterface, uint index, int propCount, out All props, int bufSize, out int length, out int params);
	public static void GetProgramResource (uint program, All programInterface, uint index, int propCount, All* props, int bufSize, int* length, int* params);
	public static void GetProgramResource (uint program, All programInterface, uint index, int propCount, All[] props, int bufSize, int[] length, int[] params);
	public static int GetProgramResourceIndex (uint program, All programInterface, System.Text.StringBuilder name);
	public static int GetProgramResourceIndex (int program, All programInterface, System.Text.StringBuilder name);
	public static int GetProgramResourceLocation (int program, All programInterface, System.Text.StringBuilder name);
	public static int GetProgramResourceLocation (uint program, All programInterface, System.Text.StringBuilder name);
	public static void GetProgramResourceName (int program, All programInterface, int index, int bufSize, int* length, System.Text.StringBuilder name);
	public static void GetProgramResourceName (uint program, All programInterface, uint index, int bufSize, out int length, System.Text.StringBuilder name);
	public static void GetProgramResourceName (int program, All programInterface, int index, int bufSize, out int length, System.Text.StringBuilder name);
	public static void GetProgramResourceName (uint program, All programInterface, uint index, int bufSize, int[] length, System.Text.StringBuilder name);
	public static void GetProgramResourceName (uint program, All programInterface, uint index, int bufSize, int* length, System.Text.StringBuilder name);
	public static void GetProgramResourceName (int program, All programInterface, int index, int bufSize, int[] length, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQuery (All target, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQuery (All target, All pname, int[] params);
	public static void GetQuery (QueryTarget target, GetQueryParam pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQuery (All target, All pname, int* params);
	public static void GetQuery (QueryTarget target, GetQueryParam pname, int[] params);
	public static void GetQuery (QueryTarget target, GetQueryParam pname, int* params);
	public static void GetQueryObject (int id, GetQueryObjectParam pname, int[] params);
	public static void GetQueryObject (int id, GetQueryObjectParam pname, out int params);
	public static void GetQueryObject (uint id, GetQueryObjectParam pname, uint[] params);
	public static void GetQueryObject (uint id, GetQueryObjectParam pname, out uint params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQueryObject (uint id, All pname, uint[] params);
	public static void GetQueryObject (int id, GetQueryObjectParam pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQueryObject (uint id, All pname, out uint params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQueryObject (uint id, All pname, uint* params);
	public static void GetQueryObject (uint id, GetQueryObjectParam pname, uint* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQueryObject (int id, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQueryObject (int id, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetQueryObject (int id, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetRenderbufferParameter (All target, All pname, int[] params);
	public static void GetRenderbufferParameter (RenderbufferTarget target, RenderbufferParameterName pname, int* params);
	public static void GetRenderbufferParameter (RenderbufferTarget target, RenderbufferParameterName pname, out int params);
	public static void GetRenderbufferParameter (RenderbufferTarget target, RenderbufferParameterName pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetRenderbufferParameter (All target, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetRenderbufferParameter (All target, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (uint sampler, All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (uint sampler, All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (uint sampler, All pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (int sampler, All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (int sampler, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (int sampler, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (int sampler, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (uint sampler, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (uint sampler, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (uint sampler, All pname, int* params);
	public static void GetSamplerParameter (uint sampler, SamplerParameterName pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (int sampler, All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSamplerParameter (int sampler, All pname, float[] params);
	public static void GetSamplerParameter (int sampler, SamplerParameterName pname, float[] params);
	public static void GetSamplerParameter (int sampler, SamplerParameterName pname, out float params);
	public static void GetSamplerParameter (int sampler, SamplerParameterName pname, float* params);
	public static void GetSamplerParameter (uint sampler, SamplerParameterName pname, float[] params);
	public static void GetSamplerParameter (uint sampler, SamplerParameterName pname, out int params);
	public static void GetSamplerParameter (uint sampler, SamplerParameterName pname, int[] params);
	public static void GetSamplerParameter (int sampler, SamplerParameterName pname, int* params);
	public static void GetSamplerParameter (int sampler, SamplerParameterName pname, out int params);
	public static void GetSamplerParameter (uint sampler, SamplerParameterName pname, float* params);
	public static void GetSamplerParameter (uint sampler, SamplerParameterName pname, out float params);
	public static void GetSamplerParameter (int sampler, SamplerParameterName pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (int shader, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (int shader, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (int shader, All pname, int[] params);
	public static void GetShader (int shader, ShaderParameter pname, int[] params);
	public static void GetShader (int shader, ShaderParameter pname, out int params);
	public static void GetShader (uint shader, ShaderParameter pname, int* params);
	public static void GetShader (uint shader, ShaderParameter pname, out int params);
	public static void GetShader (uint shader, ShaderParameter pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (uint shader, All pname, int[] params);
	public static void GetShader (int shader, ShaderParameter pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (uint shader, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShader (uint shader, All pname, out int params);
	public static void GetShaderInfoLog (int shader, out string info);
	public static string GetShaderInfoLog (int shader);
	public static void GetShaderInfoLog (uint shader, int bufsize, int* length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (uint shader, int bufsize, out int length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (uint shader, int bufsize, int[] length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (int shader, int bufsize, int* length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (int shader, int bufsize, out int length, System.Text.StringBuilder infolog);
	public static void GetShaderInfoLog (int shader, int bufsize, int[] length, System.Text.StringBuilder infolog);
	public static void GetShaderPrecisionFormat (ShaderType shadertype, ShaderPrecision precisiontype, out int range, out int precision);
	public static void GetShaderPrecisionFormat (ShaderType shadertype, ShaderPrecision precisiontype, int* range, int* precision);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShaderPrecisionFormat (All shadertype, All precisiontype, int[] range, int[] precision);
	public static void GetShaderPrecisionFormat (ShaderType shadertype, ShaderPrecision precisiontype, int[] range, int[] precision);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShaderPrecisionFormat (All shadertype, All precisiontype, int* range, int* precision);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetShaderPrecisionFormat (All shadertype, All precisiontype, out int range, out int precision);
	public static void GetShaderSource (int shader, int bufsize, int* length, System.Text.StringBuilder source);
	public static void GetShaderSource (uint shader, int bufsize, int[] length, System.Text.StringBuilder source);
	public static void GetShaderSource (uint shader, int bufsize, out int length, System.Text.StringBuilder source);
	public static void GetShaderSource (uint shader, int bufsize, int* length, System.Text.StringBuilder source);
	public static void GetShaderSource (int shader, int bufsize, out int length, System.Text.StringBuilder source);
	public static void GetShaderSource (int shader, int bufsize, int[] length, System.Text.StringBuilder source);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static string GetString (All name, int index);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static string GetString (All name, uint index);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static string GetString (All name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static string GetString (StringName name, uint index);
	public static byte GetString (StringNameIndexed name, uint index);
	public static byte GetString (StringNameIndexed name, int index);
	public static string GetString (StringName name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static string GetString (StringName name, int index);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSync (System.IntPtr sync, All pname, int bufSize, int[] length, int[] values);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSync (System.IntPtr sync, All pname, int bufSize, out int length, out int values);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetSync (System.IntPtr sync, All pname, int bufSize, int* length, int* values);
	public static void GetSync (System.IntPtr sync, SyncParameterName pname, int bufSize, int[] length, int[] values);
	public static void GetSync (System.IntPtr sync, SyncParameterName pname, int bufSize, out int length, out int values);
	public static void GetSync (System.IntPtr sync, SyncParameterName pname, int bufSize, int* length, int* values);
	public static void GetTexLevelParameter (TextureTarget target, int level, GetTextureParameter pname, float[] params);
	public static void GetTexLevelParameter (TextureTarget target, int level, GetTextureParameter pname, float* params);
	public static void GetTexLevelParameter (TextureTarget target, int level, GetTextureParameter pname, int[] params);
	public static void GetTexLevelParameter (TextureTarget target, int level, GetTextureParameter pname, out int params);
	public static void GetTexLevelParameter (TextureTarget target, int level, GetTextureParameter pname, int* params);
	public static void GetTexLevelParameter (TextureTarget target, int level, GetTextureParameter pname, out float params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, float[] params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, int* params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, out int params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, out float params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, float* params);
	public static void GetTexParameter (TextureTarget target, GetTextureParameter pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, float* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTexParameter (All target, All pname, int* params);
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, int[] length, int[] size, TransformFeedbackType[] type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, out int length, out int size, out TransformFeedbackType type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, int* length, int* size, TransformFeedbackType* type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, int[] length, int[] size, TransformFeedbackType[] type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, int* length, int* size, TransformFeedbackType* type, System.Text.StringBuilder name);
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, out int length, out int size, out TransformFeedbackType type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, int* length, int* size, All* type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, out int length, out int size, out All type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTransformFeedbackVarying (uint program, uint index, int bufSize, int[] length, int[] size, All[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, out int length, out int size, out All type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, int[] length, int[] size, All[] type, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetTransformFeedbackVarying (int program, int index, int bufSize, int* length, int* size, All* type, System.Text.StringBuilder name);
	public static void GetUniform (uint program, int location, int[] params);
	public static void GetUniform (int program, int location, int* params);
	public static void GetUniform (int program, int location, out int params);
	public static void GetUniform (int program, int location, int[] params);
	public static void GetUniform (uint program, int location, out int params);
	public static void GetUniform (uint program, int location, int* params);
	public static void GetUniform (uint program, int location, uint* params);
	public static void GetUniform (uint program, int location, out uint params);
	public static void GetUniform (uint program, int location, uint[] params);
	public static void GetUniform (uint program, int location, float* params);
	public static void GetUniform (int program, int location, float* params);
	public static void GetUniform (int program, int location, out float params);
	public static void GetUniform (int program, int location, float[] params);
	public static void GetUniform (uint program, int location, float[] params);
	public static void GetUniform (uint program, int location, out float params);
	public static int GetUniformBlockIndex (int program, System.Text.StringBuilder uniformBlockName);
	public static int GetUniformBlockIndex (uint program, System.Text.StringBuilder uniformBlockName);
	public static void GetUniformIndices (int program, int uniformCount, System.Text.StringBuilder uniformNames, int[] uniformIndices);
	public static void GetUniformIndices (int program, int uniformCount, System.Text.StringBuilder uniformNames, out int uniformIndices);
	public static void GetUniformIndices (int program, int uniformCount, System.Text.StringBuilder uniformNames, int* uniformIndices);
	public static void GetUniformIndices (uint program, int uniformCount, System.Text.StringBuilder uniformNames, uint[] uniformIndices);
	public static void GetUniformIndices (uint program, int uniformCount, System.Text.StringBuilder uniformNames, out uint uniformIndices);
	public static void GetUniformIndices (uint program, int uniformCount, System.Text.StringBuilder uniformNames, uint* uniformIndices);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int GetUniformLocation (uint program, System.Text.StringBuilder name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static int GetUniformLocation (int program, System.Text.StringBuilder name);
	public static int GetUniformLocation (uint program, string name);
	public static int GetUniformLocation (int program, string name);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, int* params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, int* params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, out int params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, int[] params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (int index, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, float[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, out float params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttrib (uint index, All pname, float* params);

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
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, out int params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, float* params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, out float params);
	public static void GetVertexAttrib (uint index, VertexAttribParameter pname, float[] params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, float* params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, out float params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, float[] params);
	public static void GetVertexAttrib (int index, VertexAttribParameter pname, int[] params);
	public static void GetVertexAttribI (uint index, VertexAttribParameter pname, uint* params);
	public static void GetVertexAttribI (uint index, VertexAttribParameter pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (uint index, All pname, uint[] params);
	public static void GetVertexAttribI (int index, VertexAttribParameter pname, int[] params);
	public static void GetVertexAttribI (int index, VertexAttribParameter pname, out int params);
	public static void GetVertexAttribI (int index, VertexAttribParameter pname, int* params);
	public static void GetVertexAttribI (uint index, VertexAttribParameter pname, uint[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (uint index, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (int index, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (int index, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (int index, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (uint index, All pname, int* params);
	public static void GetVertexAttribI (uint index, VertexAttribParameter pname, out uint params);
	public static void GetVertexAttribI (uint index, VertexAttribParameter pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (uint index, All pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (uint index, All pname, uint* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribI (uint index, All pname, out uint params);
	public static void GetVertexAttribI (uint index, VertexAttribParameter pname, out int params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (uint index, All pname, T2[] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (uint index, All pname, T2[0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (uint index, All pname, T2[0...,0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (uint index, All pname, out T2 pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer (uint index, All pname, System.IntPtr pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (int index, All pname, out T2 pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (int index, All pname, T2[0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (int index, All pname, T2[] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer (int index, All pname, System.IntPtr pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void GetVertexAttribPointer<T2> (int index, All pname, T2[0...,0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, T2[0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, T2[] pointer);
	public static void GetVertexAttribPointer (uint index, VertexAttribPointerParameter pname, System.IntPtr pointer);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, out T2 pointer);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, T2[0...,0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, T2[0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, T2[0...,0...,0...] pointer);
	public static void GetVertexAttribPointer<T2> (uint index, VertexAttribPointerParameter pname, out T2 pointer);
	public static void GetVertexAttribPointer<T2> (int index, VertexAttribPointerParameter pname, T2[] pointer);
	public static void GetVertexAttribPointer (int index, VertexAttribPointerParameter pname, System.IntPtr pointer);
	public static void Hint (HintTarget target, HintMode mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void Hint (All target, All mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void InvalidateFramebuffer (All target, int numAttachments, All* attachments);
	public static void InvalidateFramebuffer (FramebufferTarget target, int numAttachments, FramebufferAttachment* attachments);
	public static void InvalidateFramebuffer (FramebufferTarget target, int numAttachments, ref FramebufferAttachment attachments);
	public static void InvalidateFramebuffer (FramebufferTarget target, int numAttachments, FramebufferAttachment[] attachments);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void InvalidateFramebuffer (All target, int numAttachments, ref All attachments);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void InvalidateFramebuffer (All target, int numAttachments, All[] attachments);
	public static void InvalidateSubFramebuffer (FramebufferTarget target, int numAttachments, FramebufferAttachment[] attachments, int x, int y, int width, int height);
	public static void InvalidateSubFramebuffer (FramebufferTarget target, int numAttachments, FramebufferAttachment* attachments, int x, int y, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void InvalidateSubFramebuffer (All target, int numAttachments, All* attachments, int x, int y, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void InvalidateSubFramebuffer (All target, int numAttachments, ref All attachments, int x, int y, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void InvalidateSubFramebuffer (All target, int numAttachments, All[] attachments, int x, int y, int width, int height);
	public static void InvalidateSubFramebuffer (FramebufferTarget target, int numAttachments, ref FramebufferAttachment attachments, int x, int y, int width, int height);
	public static bool IsBuffer (uint buffer);
	public static bool IsBuffer (int buffer);
	public static bool IsEnabled (EnableCap cap);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static bool IsEnabled (All cap);
	public static bool IsFramebuffer (uint framebuffer);
	public static bool IsFramebuffer (int framebuffer);
	public static bool IsProgram (int program);
	public static bool IsProgram (uint program);
	public static bool IsProgramPipeline (uint pipeline);
	public static bool IsProgramPipeline (int pipeline);
	public static bool IsQuery (uint id);
	public static bool IsQuery (int id);
	public static bool IsRenderbuffer (int renderbuffer);
	public static bool IsRenderbuffer (uint renderbuffer);
	public static bool IsSampler (int sampler);
	public static bool IsSampler (uint sampler);
	public static bool IsShader (uint shader);
	public static bool IsShader (int shader);
	public static bool IsSync (System.IntPtr sync);
	public static bool IsTexture (int texture);
	public static bool IsTexture (uint texture);
	public static bool IsTransformFeedback (uint id);
	public static bool IsTransformFeedback (int id);
	public static bool IsVertexArray (int array);
	public static bool IsVertexArray (uint array);
	public static void LineWidth (float width);
	public static void LinkProgram (int program);
	public static void LinkProgram (uint program);
	public static System.IntPtr MapBufferRange (BufferTarget target, System.IntPtr offset, System.IntPtr length, BufferAccessMask access);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static System.IntPtr MapBufferRange (All target, System.IntPtr offset, System.IntPtr length, uint access);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static System.IntPtr MapBufferRange (All target, System.IntPtr offset, System.IntPtr length, int access);
	public static void MemoryBarrier (int barriers);
	public static void MemoryBarrier (uint barriers);
	public static void MemoryBarrierByRegion (uint barriers);
	public static void MemoryBarrierByRegion (int barriers);
	public static void PauseTransformFeedback ();

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void PixelStore (All pname, int param);
	public static void PixelStore (PixelStoreParameter pname, int param);
	public static void PolygonOffset (float factor, float units);
	public static void ProgramBinary<T2> (uint program, All binaryFormat, T2[0...,0...] binary, int length);
	public static void ProgramBinary<T2> (int program, All binaryFormat, out T2 binary, int length);
	public static void ProgramBinary<T2> (int program, All binaryFormat, T2[0...,0...,0...] binary, int length);
	public static void ProgramBinary<T2> (int program, All binaryFormat, T2[0...,0...] binary, int length);
	public static void ProgramBinary<T2> (int program, All binaryFormat, T2[] binary, int length);
	public static void ProgramBinary (int program, All binaryFormat, System.IntPtr binary, int length);
	public static void ProgramBinary<T2> (uint program, All binaryFormat, T2[] binary, int length);
	public static void ProgramBinary (uint program, All binaryFormat, System.IntPtr binary, int length);
	public static void ProgramBinary<T2> (uint program, All binaryFormat, out T2 binary, int length);
	public static void ProgramBinary<T2> (uint program, All binaryFormat, T2[0...,0...,0...] binary, int length);
	public static void ProgramParameter (uint program, ProgramParameterName pname, int value);
	public static void ProgramParameter (int program, ProgramParameterName pname, int value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ProgramParameter (int program, All pname, int value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ProgramParameter (uint program, All pname, int value);
	public static void ProgramUniform1 (uint program, int location, int count, ref float value);
	public static void ProgramUniform1 (int program, int location, int count, float* value);
	public static void ProgramUniform1 (uint program, int location, int count, float[] value);
	public static void ProgramUniform1 (uint program, int location, int count, uint[] value);
	public static void ProgramUniform1 (int program, int location, int count, ref float value);
	public static void ProgramUniform1 (int program, int location, float v0);
	public static void ProgramUniform1 (uint program, int location, float v0);
	public static void ProgramUniform1 (int program, int location, int count, float[] value);
	public static void ProgramUniform1 (uint program, int location, int count, float* value);
	public static void ProgramUniform1 (uint program, int location, int count, uint* value);
	public static void ProgramUniform1 (uint program, int location, uint v0);
	public static void ProgramUniform1 (uint program, int location, int count, int* value);
	public static void ProgramUniform1 (uint program, int location, int count, ref int value);
	public static void ProgramUniform1 (uint program, int location, int count, int[] value);
	public static void ProgramUniform1 (int program, int location, int v0);
	public static void ProgramUniform1 (uint program, int location, int count, ref uint value);
	public static void ProgramUniform1 (uint program, int location, int v0);
	public static void ProgramUniform1 (int program, int location, int count, int[] value);
	public static void ProgramUniform1 (int program, int location, int count, int* value);
	public static void ProgramUniform1 (int program, int location, int count, ref int value);
	public static void ProgramUniform2 (int program, int location, float v0, float v1);
	public static void ProgramUniform2 (uint program, int location, float v0, float v1);
	public static void ProgramUniform2 (int program, int location, int count, float[] value);
	public static void ProgramUniform2 (int program, int location, int count, ref float value);
	public static void ProgramUniform2 (int program, int location, int count, float* value);
	public static void ProgramUniform2 (uint program, int location, int count, ref float value);
	public static void ProgramUniform2 (uint program, int location, int count, float* value);
	public static void ProgramUniform2 (uint program, int location, int count, float[] value);
	public static void ProgramUniform2 (uint program, int location, int count, uint[] value);
	public static void ProgramUniform2 (uint program, int location, uint v0, uint v1);
	public static void ProgramUniform2 (uint program, int location, int count, int* value);
	public static void ProgramUniform2 (uint program, int location, int count, int[] value);
	public static void ProgramUniform2 (int program, int location, int count, int* value);
	public static void ProgramUniform2 (uint program, int location, int count, uint* value);
	public static void ProgramUniform2 (uint program, int location, int count, ref uint value);
	public static void ProgramUniform2 (int program, int location, int v0, int v1);
	public static void ProgramUniform2 (uint program, int location, int v0, int v1);
	public static void ProgramUniform2 (int program, int location, int count, int[] value);
	public static void ProgramUniform3 (uint program, int location, uint v0, uint v1, uint v2);
	public static void ProgramUniform3 (uint program, int location, int count, uint[] value);
	public static void ProgramUniform3 (uint program, int location, int count, ref uint value);
	public static void ProgramUniform3 (uint program, int location, int count, uint* value);
	public static void ProgramUniform3 (uint program, int location, int count, int[] value);
	public static void ProgramUniform3 (uint program, int location, int count, int* value);
	public static void ProgramUniform3 (int program, int location, int count, float* value);
	public static void ProgramUniform3 (uint program, int location, int count, float[] value);
	public static void ProgramUniform3 (uint program, int location, int v0, int v1, int v2);
	public static void ProgramUniform3 (uint program, int location, int count, ref float value);
	public static void ProgramUniform3 (uint program, int location, int count, float* value);
	public static void ProgramUniform3 (int program, int location, int v0, int v1, int v2);
	public static void ProgramUniform3 (int program, int location, int count, ref float value);
	public static void ProgramUniform3 (uint program, int location, int count, ref int value);
	public static void ProgramUniform3 (int program, int location, int count, int* value);
	public static void ProgramUniform3 (int program, int location, int count, ref int value);
	public static void ProgramUniform3 (int program, int location, int count, int[] value);
	public static void ProgramUniform3 (int program, int location, float v0, float v1, float v2);
	public static void ProgramUniform3 (uint program, int location, float v0, float v1, float v2);
	public static void ProgramUniform3 (int program, int location, int count, float[] value);
	public static void ProgramUniform4 (uint program, int location, uint v0, uint v1, uint v2, uint v3);
	public static void ProgramUniform4 (uint program, int location, int count, uint[] value);
	public static void ProgramUniform4 (uint program, int location, int count, ref uint value);
	public static void ProgramUniform4 (uint program, int location, int count, uint* value);
	public static void ProgramUniform4 (uint program, int location, int count, ref float value);
	public static void ProgramUniform4 (uint program, int location, int count, int* value);
	public static void ProgramUniform4 (int program, int location, int count, int[] value);
	public static void ProgramUniform4 (int program, int location, int count, float* value);
	public static void ProgramUniform4 (uint program, int location, int count, float[] value);
	public static void ProgramUniform4 (uint program, int location, int count, float* value);
	public static void ProgramUniform4 (int program, int location, int v0, int v1, int v2, int v3);
	public static void ProgramUniform4 (uint program, int location, int v0, int v1, int v2, int v3);
	public static void ProgramUniform4 (int program, int location, int count, ref float value);
	public static void ProgramUniform4 (uint program, int location, int count, ref int value);
	public static void ProgramUniform4 (uint program, int location, int count, int[] value);
	public static void ProgramUniform4 (int program, int location, int count, int* value);
	public static void ProgramUniform4 (int program, int location, int count, ref int value);
	public static void ProgramUniform4 (int program, int location, float v0, float v1, float v2, float v3);
	public static void ProgramUniform4 (uint program, int location, float v0, float v1, float v2, float v3);
	public static void ProgramUniform4 (int program, int location, int count, float[] value);
	public static void ProgramUniformMatrix2 (uint program, int location, int count, bool transpose, ref float value);
	public static void ProgramUniformMatrix2 (uint program, int location, int count, bool transpose, float[] value);
	public static void ProgramUniformMatrix2 (int program, int location, int count, bool transpose, float[] value);
	public static void ProgramUniformMatrix2 (int program, int location, int count, bool transpose, ref float value);
	public static void ProgramUniformMatrix2 (uint program, int location, int count, bool transpose, float* value);
	public static void ProgramUniformMatrix2 (int program, int location, int count, bool transpose, float* value);
	public static void ProgramUniformMatrix2x3 (int program, int location, int count, bool transpose, float* value);
	public static void ProgramUniformMatrix2x3 (uint program, int location, int count, bool transpose, float[] value);
	public static void ProgramUniformMatrix2x3 (int program, int location, int count, bool transpose, ref float value);
	public static void ProgramUniformMatrix2x3 (int program, int location, int count, bool transpose, float[] value);
	public static void ProgramUniformMatrix2x3 (uint program, int location, int count, bool transpose, float* value);
	public static void ProgramUniformMatrix2x3 (uint program, int location, int count, bool transpose, ref float value);
	public static void ProgramUniformMatrix2x4 (int program, int location, int count, bool transpose, float* value);
	public static void ProgramUniformMatrix2x4 (int program, int location, int count, bool transpose, float[] value);
	public static void ProgramUniformMatrix2x4 (int program, int location, int count, bool transpose, ref float value);
	public static void ProgramUniformMatrix2x4 (uint program, int location, int count, bool transpose, float[] value);
	public static void ProgramUniformMatrix2x4 (uint program, int location, int count, bool transpose, ref float value);
	public static void ProgramUniformMatrix2x4 (uint program, int location, int count, bool transpose, float* value);
	public static void ProgramUniformMatrix3 (int program, int location, int count, bool transpose, float[] value);
	public static void ProgramUniformMatrix3 (int program, int location, int count, bool transpose, ref float value);
	public static void ProgramUniformMatrix3 (int program, int location, int count, bool transpose, float* value);
	public static void ProgramUniformMatrix3 (uint program, int location, int count, bool transpose, float[] value);
	public static void ProgramUniformMatrix3 (uint program, int location, int count, bool transpose, float* value);
	public static void ProgramUniformMatrix3 (uint program, int location, int count, bool transpose, ref float value);
	public static void ProgramUniformMatrix3x2 (uint program, int location, int count, bool transpose, float[] value);
	public static void ProgramUniformMatrix3x2 (uint program, int location, int count, bool transpose, float* value);
	public static void ProgramUniformMatrix3x2 (uint program, int location, int count, bool transpose, ref float value);
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
	public static void ProgramUniformMatrix4x2 (int program, int location, int count, bool transpose, float* value);
	public static void ProgramUniformMatrix4x2 (uint program, int location, int count, bool transpose, float[] value);
	public static void ProgramUniformMatrix4x2 (int program, int location, int count, bool transpose, ref float value);
	public static void ProgramUniformMatrix4x2 (int program, int location, int count, bool transpose, float[] value);
	public static void ProgramUniformMatrix4x3 (int program, int location, int count, bool transpose, float* value);
	public static void ProgramUniformMatrix4x3 (int program, int location, int count, bool transpose, float[] value);
	public static void ProgramUniformMatrix4x3 (uint program, int location, int count, bool transpose, ref float value);
	public static void ProgramUniformMatrix4x3 (uint program, int location, int count, bool transpose, float* value);
	public static void ProgramUniformMatrix4x3 (uint program, int location, int count, bool transpose, float[] value);
	public static void ProgramUniformMatrix4x3 (int program, int location, int count, bool transpose, ref float value);
	public static void ReadBuffer (ReadBufferMode mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadBuffer (All mode);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, T6[0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, T6[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, out T6 pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels (int x, int y, int width, int height, All format, All type, System.IntPtr pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, out T6 pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, T6[0...,0...,0...] pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, T6[0...,0...] pixels);
	public static void ReadPixels<T6> (int x, int y, int width, int height, PixelFormat format, PixelType type, T6[] pixels);
	public static void ReadPixels (int x, int y, int width, int height, PixelFormat format, PixelType type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ReadPixels<T6> (int x, int y, int width, int height, All format, All type, T6[] pixels);
	public static void ReleaseShaderCompiler ();

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void RenderbufferStorage (All target, All internalformat, int width, int height);
	public static void RenderbufferStorage (RenderbufferTarget target, RenderbufferInternalFormat internalformat, int width, int height);
	public static void RenderbufferStorageMultisample (RenderbufferTarget target, int samples, RenderbufferInternalFormat internalformat, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void RenderbufferStorageMultisample (All target, int samples, All internalformat, int width, int height);
	public static void ResumeTransformFeedback ();
	public static void SampleCoverage (float value, bool invert);
	public static void SampleMask (int maskNumber, int mask);
	public static void SampleMask (uint maskNumber, uint mask);
	public static void SamplerParameter (uint sampler, SamplerParameterName pname, float param);
	public static void SamplerParameter (int sampler, SamplerParameterName pname, float param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (int sampler, All pname, int param);
	public static void SamplerParameter (int sampler, SamplerParameterName pname, float[] param);
	public static void SamplerParameter (uint sampler, SamplerParameterName pname, int* param);
	public static void SamplerParameter (uint sampler, SamplerParameterName pname, int[] param);
	public static void SamplerParameter (int sampler, SamplerParameterName pname, int* param);
	public static void SamplerParameter (int sampler, SamplerParameterName pname, int[] param);
	public static void SamplerParameter (uint sampler, SamplerParameterName pname, int param);
	public static void SamplerParameter (int sampler, SamplerParameterName pname, int param);
	public static void SamplerParameter (uint sampler, SamplerParameterName pname, float* param);
	public static void SamplerParameter (uint sampler, SamplerParameterName pname, float[] param);
	public static void SamplerParameter (int sampler, SamplerParameterName pname, float* param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (int sampler, All pname, int* param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (int sampler, All pname, float* param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (int sampler, All pname, float[] param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (uint sampler, All pname, int* param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (uint sampler, All pname, int[] param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (uint sampler, All pname, float param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (int sampler, All pname, int[] param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (uint sampler, All pname, int param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (uint sampler, All pname, float[] param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (int sampler, All pname, float param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void SamplerParameter (uint sampler, All pname, float* param);
	public static void Scissor (int x, int y, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref int shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref int shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, int* shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int* shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int* shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref int shaders, All binaryformat, out T3 binary, int length);
	public static void ShaderBinary (int n, uint* shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, int[] shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int[] shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int[] shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int[] shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int[] shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, ref int shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref int shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref uint shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int* shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint* shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint* shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint* shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, uint* shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref uint shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref uint shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, ref uint shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, ref uint shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint* shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, int* shaders, All binaryformat, out T3 binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary (int n, uint[] shaders, All binaryformat, System.IntPtr binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint[] shaders, All binaryformat, T3[] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint[] shaders, All binaryformat, T3[0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint[] shaders, All binaryformat, T3[0...,0...,0...] binary, int length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void ShaderBinary<T3> (int n, uint[] shaders, All binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, uint* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary (int n, int* shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary (int n, int[] shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, int[] shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary (int n, ref int shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, ref int shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary<T3> (int n, int* shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, ref uint shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary (int n, ref uint shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, out T3 binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, T3[] binary, int length);
	public static void ShaderBinary (int n, uint[] shaders, ShaderBinaryFormat binaryformat, System.IntPtr binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...] binary, int length);
	public static void ShaderBinary<T3> (int n, uint[] shaders, ShaderBinaryFormat binaryformat, T3[0...,0...,0...] binary, int length);
	public static void ShaderSource (int shader, int count, string[] string, int* length);
	public static void ShaderSource (uint shader, int count, string[] string, ref int length);
	public static void ShaderSource (uint shader, int count, string[] string, int[] length);
	public static void ShaderSource (int shader, int count, string[] string, ref int length);
	public static void ShaderSource (int shader, int count, string[] string, int[] length);
	public static void ShaderSource (int shader, string string);
	public static void ShaderSource (uint shader, int count, string[] string, int* length);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilFunc (All func, int ref, int mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilFunc (All func, int ref, uint mask);
	public static void StencilFunc (StencilFunction func, int ref, int mask);
	public static void StencilFunc (StencilFunction func, int ref, uint mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilFuncSeparate (All face, All func, int ref, int mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilFuncSeparate (All face, All func, int ref, uint mask);
	public static void StencilFuncSeparate (CullFaceMode face, StencilFunction func, int ref, uint mask);
	public static void StencilFuncSeparate (CullFaceMode face, StencilFunction func, int ref, int mask);
	public static void StencilMask (uint mask);
	public static void StencilMask (int mask);
	public static void StencilMaskSeparate (CullFaceMode face, int mask);
	public static void StencilMaskSeparate (CullFaceMode face, uint mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilMaskSeparate (All face, uint mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilMaskSeparate (All face, int mask);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilOp (All fail, All zfail, All zpass);
	public static void StencilOp (StencilOp fail, StencilOp zfail, StencilOp zpass);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void StencilOpSeparate (All face, All fail, All zfail, All zpass);
	public static void StencilOpSeparate (CullFaceMode face, StencilOp fail, StencilOp zfail, StencilOp zpass);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, out T8 pixels);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, T8[0...,0...,0...] pixels);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, T8[0...,0...] pixels);
	public static void TexImage2D<T8> (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, T8[] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, T8[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D (All target, int level, int internalformat, int width, int height, int border, All format, All type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, T8[] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, T8[0...,0...] pixels);
	public static void TexImage2D (TextureTarget target, int level, PixelInternalFormat internalformat, int width, int height, int border, PixelFormat format, PixelType type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage2D<T8> (All target, int level, int internalformat, int width, int height, int border, All format, All type, out T8 pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage3D<T9> (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, T9[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage3D<T9> (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, out T9 pixels);
	public static void TexImage3D (TextureTarget3D target, int level, TextureComponentCount internalformat, int width, int height, int depth, int border, PixelFormat format, PixelType type, System.IntPtr pixels);
	public static void TexImage3D<T9> (TextureTarget3D target, int level, TextureComponentCount internalformat, int width, int height, int depth, int border, PixelFormat format, PixelType type, T9[] pixels);
	public static void TexImage3D<T9> (TextureTarget3D target, int level, TextureComponentCount internalformat, int width, int height, int depth, int border, PixelFormat format, PixelType type, T9[0...,0...] pixels);
	public static void TexImage3D<T9> (TextureTarget3D target, int level, TextureComponentCount internalformat, int width, int height, int depth, int border, PixelFormat format, PixelType type, T9[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage3D<T9> (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, T9[0...,0...] pixels);
	public static void TexImage3D<T9> (TextureTarget3D target, int level, TextureComponentCount internalformat, int width, int height, int depth, int border, PixelFormat format, PixelType type, out T9 pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage3D<T9> (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, T9[] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexImage3D (All target, int level, int internalformat, int width, int height, int depth, int border, All format, All type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, int param);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, float param);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, float[] params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, float* params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, int param);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, float* params);
	public static void TexParameter (TextureTarget target, TextureParameterName pname, int* params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, int[] params);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, float param);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexParameter (All target, All pname, float[] params);
	public static void TexStorage2D (TextureTarget2D target, int levels, SizedInternalFormat internalformat, int width, int height);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexStorage2D (All target, int levels, All internalformat, int width, int height);
	public static void TexStorage2DMultisample (All target, int samples, All internalformat, int width, int height, bool fixedsamplelocations);
	public static void TexStorage3D (TextureTarget3D target, int levels, SizedInternalFormat internalformat, int width, int height, int depth);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexStorage3D (All target, int levels, All internalformat, int width, int height, int depth);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, out T8 pixels);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, T8[0...,0...] pixels);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, T8[] pixels);
	public static void TexSubImage2D (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, System.IntPtr pixels);
	public static void TexSubImage2D<T8> (TextureTarget target, int level, int xoffset, int yoffset, int width, int height, PixelFormat format, PixelType type, T8[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, T8[] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, T8[0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, T8[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage2D<T8> (All target, int level, int xoffset, int yoffset, int width, int height, All format, All type, out T8 pixels);
	public static void TexSubImage3D (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, PixelFormat format, PixelType type, System.IntPtr pixels);
	public static void TexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, PixelFormat format, PixelType type, T10[] pixels);
	public static void TexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, PixelFormat format, PixelType type, out T10 pixels);
	public static void TexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, PixelFormat format, PixelType type, T10[0...,0...,0...] pixels);
	public static void TexSubImage3D<T10> (TextureTarget3D target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, PixelFormat format, PixelType type, T10[0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, T10[0...,0...,0...] pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage3D<T10> (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, out T10 pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TexSubImage3D (All target, int level, int xoffset, int yoffset, int zoffset, int width, int height, int depth, All format, All type, System.IntPtr pixels);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void TransformFeedbackVaryings (int program, int count, string varyings, All bufferMode);
	public static void TransformFeedbackVaryings (uint program, int count, string varyings, All bufferMode);
	public static void TransformFeedbackVaryings (uint program, int count, string varyings, TransformFeedbackMode bufferMode);
	public static void TransformFeedbackVaryings (int program, int count, string varyings, TransformFeedbackMode bufferMode);
	public static void Uniform1 (int location, int count, ref float v);
	public static void Uniform1 (int location, int count, float[] v);
	public static void Uniform1 (int location, float x);
	public static void Uniform1 (int location, int count, int[] v);
	public static void Uniform1 (int location, int count, float* v);
	public static void Uniform1 (int location, int count, ref uint value);
	public static void Uniform1 (int location, int count, uint[] value);
	public static void Uniform1 (int location, uint v0);
	public static void Uniform1 (int location, int count, int* v);
	public static void Uniform1 (int location, int count, ref int v);
	public static void Uniform1 (int location, int count, uint* value);
	public static void Uniform1 (int location, int x);
	public static void Uniform2 (int location, ref OpenTK.Vector2 vector);
	public static void Uniform2 (int location, OpenTK.Vector2 vector);
	public static void Uniform2 (int location, int count, uint* value);
	public static void Uniform2 (int location, int count, ref uint value);
	public static void Uniform2 (int location, int count, uint[] value);
	public static void Uniform2 (int location, uint v0, uint v1);
	public static void Uniform2 (int location, int count, int* v);
	public static void Uniform2 (int location, int count, int[] v);
	public static void Uniform2 (int location, float x, float y);
	public static void Uniform2 (int location, int count, float[] v);
	public static void Uniform2 (int location, int count, ref float v);
	public static void Uniform2 (int location, int count, float* v);
	public static void Uniform2 (int location, int x, int y);
	public static void Uniform3 (int location, uint v0, uint v1, uint v2);
	public static void Uniform3 (int location, int count, uint[] value);
	public static void Uniform3 (int location, int count, ref uint value);
	public static void Uniform3 (int location, int count, uint* value);
	public static void Uniform3 (int location, OpenTK.Vector3 vector);
	public static void Uniform3 (int location, ref OpenTK.Vector3 vector);
	public static void Uniform3 (int location, int count, int* v);
	public static void Uniform3 (int location, int count, float[] v);
	public static void Uniform3 (int location, float x, float y, float z);
	public static void Uniform3 (int location, int count, ref float v);
	public static void Uniform3 (int location, int count, float* v);
	public static void Uniform3 (int location, int x, int y, int z);
	public static void Uniform3 (int location, int count, int[] v);
	public static void Uniform3 (int location, int count, ref int v);
	public static void Uniform4 (int location, int count, uint[] value);
	public static void Uniform4 (int location, int count, uint* value);
	public static void Uniform4 (int location, OpenTK.Quaternion quaternion);
	public static void Uniform4 (int location, OpenTK.Graphics.Color4 color);
	public static void Uniform4 (int location, OpenTK.Vector4 vector);
	public static void Uniform4 (int location, ref OpenTK.Vector4 vector);
	public static void Uniform4 (int location, uint v0, uint v1, uint v2, uint v3);
	public static void Uniform4 (int location, float x, float y, float z, float w);
	public static void Uniform4 (int location, int count, float[] v);
	public static void Uniform4 (int location, int count, ref float v);
	public static void Uniform4 (int location, int count, float* v);
	public static void Uniform4 (int location, int x, int y, int z, int w);
	public static void Uniform4 (int location, int count, int[] v);
	public static void Uniform4 (int location, int count, ref int v);
	public static void Uniform4 (int location, int count, int* v);
	public static void Uniform4 (int location, int count, ref uint value);
	public static void UniformBlockBinding (int program, int uniformBlockIndex, int uniformBlockBinding);
	public static void UniformBlockBinding (uint program, uint uniformBlockIndex, uint uniformBlockBinding);
	public static void UniformMatrix2 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix2 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix2 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix2x3 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix2x3 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix2x3 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix2x4 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix2x4 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix2x4 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix3 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix3 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix3 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix3x2 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix3x2 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix3x2 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix3x4 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix3x4 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix3x4 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix4 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix4 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix4 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix4 (int location, bool transpose, ref OpenTK.Matrix4 matrix);
	public static void UniformMatrix4x2 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix4x2 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix4x2 (int location, int count, bool transpose, float[] value);
	public static void UniformMatrix4x3 (int location, int count, bool transpose, float* value);
	public static void UniformMatrix4x3 (int location, int count, bool transpose, ref float value);
	public static void UniformMatrix4x3 (int location, int count, bool transpose, float[] value);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static bool UnmapBuffer (All target);
	public static bool UnmapBuffer (BufferTarget target);
	public static void UseProgram (int program);
	public static void UseProgram (uint program);
	public static void UseProgramStages (uint pipeline, uint stages, uint program);
	public static void UseProgramStages (int pipeline, int stages, int program);
	public static void ValidateProgram (uint program);
	public static void ValidateProgram (int program);
	public static void ValidateProgramPipeline (int pipeline);
	public static void ValidateProgramPipeline (uint pipeline);
	public static void VertexAttrib1 (uint indx, float[] values);
	public static void VertexAttrib1 (uint indx, float* values);
	public static void VertexAttrib1 (int indx, float* values);
	public static void VertexAttrib1 (int indx, float[] values);
	public static void VertexAttrib1 (uint indx, float x);
	public static void VertexAttrib1 (int indx, float x);
	public static void VertexAttrib2 (uint indx, float[] values);
	public static void VertexAttrib2 (uint indx, ref float values);
	public static void VertexAttrib2 (uint indx, float* values);
	public static void VertexAttrib2 (int index, ref OpenTK.Vector2 v);
	public static void VertexAttrib2 (int index, OpenTK.Vector2 v);
	public static void VertexAttrib2 (int indx, float* values);
	public static void VertexAttrib2 (int indx, float x, float y);
	public static void VertexAttrib2 (uint indx, float x, float y);
	public static void VertexAttrib2 (int indx, float[] values);
	public static void VertexAttrib2 (int indx, ref float values);
	public static void VertexAttrib3 (uint indx, ref float values);
	public static void VertexAttrib3 (uint indx, float* values);
	public static void VertexAttrib3 (int index, ref OpenTK.Vector3 v);
	public static void VertexAttrib3 (int index, OpenTK.Vector3 v);
	public static void VertexAttrib3 (uint indx, float[] values);
	public static void VertexAttrib3 (int indx, float x, float y, float z);
	public static void VertexAttrib3 (uint indx, float x, float y, float z);
	public static void VertexAttrib3 (int indx, float[] values);
	public static void VertexAttrib3 (int indx, ref float values);
	public static void VertexAttrib3 (int indx, float* values);
	public static void VertexAttrib4 (int index, ref OpenTK.Vector4 v);
	public static void VertexAttrib4 (int index, OpenTK.Vector4 v);
	public static void VertexAttrib4 (uint indx, float* values);
	public static void VertexAttrib4 (uint indx, ref float values);
	public static void VertexAttrib4 (int indx, ref float values);
	public static void VertexAttrib4 (uint indx, float x, float y, float z, float w);
	public static void VertexAttrib4 (int indx, float x, float y, float z, float w);
	public static void VertexAttrib4 (int indx, float[] values);
	public static void VertexAttrib4 (int indx, float* values);
	public static void VertexAttrib4 (uint indx, float[] values);
	public static void VertexAttribBinding (int attribindex, int bindingindex);
	public static void VertexAttribBinding (uint attribindex, uint bindingindex);
	public static void VertexAttribDivisor (uint index, uint divisor);
	public static void VertexAttribDivisor (int index, int divisor);
	public static void VertexAttribFormat (uint attribindex, int size, All type, bool normalized, uint relativeoffset);
	public static void VertexAttribFormat (int attribindex, int size, All type, bool normalized, int relativeoffset);
	public static void VertexAttribI4 (int index, int* v);
	public static void VertexAttribI4 (int index, ref int v);
	public static void VertexAttribI4 (int index, int[] v);
	public static void VertexAttribI4 (uint index, int x, int y, int z, int w);
	public static void VertexAttribI4 (int index, int x, int y, int z, int w);
	public static void VertexAttribI4 (uint index, uint* v);
	public static void VertexAttribI4 (uint index, int[] v);
	public static void VertexAttribI4 (uint index, ref int v);
	public static void VertexAttribI4 (uint index, int* v);
	public static void VertexAttribI4 (uint index, uint x, uint y, uint z, uint w);
	public static void VertexAttribI4 (uint index, uint[] v);
	public static void VertexAttribI4 (uint index, ref uint v);
	public static void VertexAttribIFormat (uint attribindex, int size, All type, uint relativeoffset);
	public static void VertexAttribIFormat (int attribindex, int size, All type, int relativeoffset);
	public static void VertexAttribIPointer (uint index, int size, VertexAttribIntegerType type, int stride, System.IntPtr pointer);
	public static void VertexAttribIPointer<T4> (int index, int size, VertexAttribIntegerType type, int stride, out T4 pointer);
	public static void VertexAttribIPointer<T4> (int index, int size, VertexAttribIntegerType type, int stride, T4[0...,0...,0...] pointer);
	public static void VertexAttribIPointer<T4> (uint index, int size, VertexAttribIntegerType type, int stride, T4[] pointer);
	public static void VertexAttribIPointer<T4> (uint index, int size, VertexAttribIntegerType type, int stride, T4[0...,0...] pointer);
	public static void VertexAttribIPointer<T4> (uint index, int size, VertexAttribIntegerType type, int stride, T4[0...,0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (int index, int size, All type, int stride, T4[0...,0...,0...] pointer);
	public static void VertexAttribIPointer<T4> (uint index, int size, VertexAttribIntegerType type, int stride, out T4 pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (uint index, int size, All type, int stride, out T4 pointer);
	public static void VertexAttribIPointer (int index, int size, VertexAttribIntegerType type, int stride, System.IntPtr pointer);
	public static void VertexAttribIPointer<T4> (int index, int size, VertexAttribIntegerType type, int stride, T4[] pointer);
	public static void VertexAttribIPointer<T4> (int index, int size, VertexAttribIntegerType type, int stride, T4[0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (int index, int size, All type, int stride, T4[] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (int index, int size, All type, int stride, T4[0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer (int index, int size, All type, int stride, System.IntPtr pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (uint index, int size, All type, int stride, T4[0...,0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (uint index, int size, All type, int stride, T4[0...,0...] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (uint index, int size, All type, int stride, T4[] pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer (uint index, int size, All type, int stride, System.IntPtr pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribIPointer<T4> (int index, int size, All type, int stride, out T4 pointer);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, out T5 ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, T5[0...,0...,0...] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer (int indx, int size, All type, bool normalized, int stride, System.IntPtr ptr);
	public static void VertexAttribPointer (int index, int size, VertexAttribPointerType type, bool normalized, int stride, int offset);
	public static void VertexAttribPointer (uint index, int size, VertexAttribPointerType type, bool normalized, int stride, int offset);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...] ptr);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...,0...] ptr);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, out T5 ptr);
	public static void VertexAttribPointer<T5> (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, T5[] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, T5[0...,0...] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, out T5 ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer (uint indx, int size, All type, bool normalized, int stride, System.IntPtr ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, T5[] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (uint indx, int size, All type, bool normalized, int stride, T5[0...,0...] ptr);

	[Obsolete ("Use the overload with strongly typed enumerations")]
	public static void VertexAttribPointer<T5> (int indx, int size, All type, bool normalized, int stride, T5[0...,0...,0...] ptr);
	public static void VertexAttribPointer (uint indx, int size, VertexAttribPointerType type, bool normalized, int stride, System.IntPtr ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, out T5 ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...,0...] ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[0...,0...] ptr);
	public static void VertexAttribPointer<T5> (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, T5[] ptr);
	public static void VertexAttribPointer (int indx, int size, VertexAttribPointerType type, bool normalized, int stride, System.IntPtr ptr);
	public static void VertexBindingDivisor (int bindingindex, int divisor);
	public static void VertexBindingDivisor (uint bindingindex, uint divisor);
	public static void Viewport (System.Drawing.Rectangle rectangle);
	public static void Viewport (System.Drawing.Point location, System.Drawing.Size size);
	public static void Viewport (System.Drawing.Size size);
	public static void Viewport (int x, int y, int width, int height);
	public static void WaitSync (System.IntPtr sync, int flags, long timeout);
	public static void WaitSync (System.IntPtr sync, uint flags, ulong timeout);
}
```

### New Type OpenTK.Graphics.ES31.HintMode

```
[Serializable]
public enum HintMode {
	DontCare = 4352,
	Fastest = 4353,
	Nicest = 4354,
}
```

### New Type OpenTK.Graphics.ES31.HintTarget

```
[Serializable]
public enum HintTarget {
	FragmentShaderDerivativeHint = 35723,
	GenerateMipmapHint = 33170,
}
```

### New Type OpenTK.Graphics.ES31.ImageTarget

```
[Serializable]
public enum ImageTarget {
	Renderbuffer = 36161,
}
```

### New Type OpenTK.Graphics.ES31.InternalFormatParameter

```
[Serializable]
public enum InternalFormatParameter {
	NumSampleCounts = 37760,
	Samples = 32937,
}
```

### New Type OpenTK.Graphics.ES31.OpenGlescoreVersions

```
[Serializable]
public enum OpenGlescoreVersions {
	EsVersion20 = 1,
	EsVersion30 = 1,
	EsVersion31 = 1,
}
```

### New Type OpenTK.Graphics.ES31.OpenGlEsCoreVersions

```
[Serializable]
public enum OpenGlEsCoreVersions {
	EsVersion20 = 1,
	EsVersion30 = 1,
}
```

### New Type OpenTK.Graphics.ES31.PixelFormat

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

### New Type OpenTK.Graphics.ES31.PixelInternalFormat

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

### New Type OpenTK.Graphics.ES31.PixelStoreParameter

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

### New Type OpenTK.Graphics.ES31.PixelType

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

### New Type OpenTK.Graphics.ES31.PrimitiveType

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

### New Type OpenTK.Graphics.ES31.ProgramParameter

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

### New Type OpenTK.Graphics.ES31.ProgramParameterName

```
[Serializable]
public enum ProgramParameterName {
	ProgramBinaryRetrievableHint = 33367,
}
```

### New Type OpenTK.Graphics.ES31.QueryTarget

```
[Serializable]
public enum QueryTarget {
	AnySamplesPassed = 35887,
	AnySamplesPassedConservative = 36202,
	TransformFeedbackPrimitivesWritten = 35976,
}
```

### New Type OpenTK.Graphics.ES31.ReadBufferMode

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

### New Type OpenTK.Graphics.ES31.ReadFormat

```
[Serializable]
public enum ReadFormat {
	ImplementationColorReadFormat = 35739,
	ImplementationColorReadType = 35738,
}
```

### New Type OpenTK.Graphics.ES31.RenderbufferInternalFormat

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

### New Type OpenTK.Graphics.ES31.RenderbufferParameterName

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

### New Type OpenTK.Graphics.ES31.RenderbufferTarget

```
[Serializable]
public enum RenderbufferTarget {
	Renderbuffer = 36161,
}
```

### New Type OpenTK.Graphics.ES31.SamplerParameterName

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

### New Type OpenTK.Graphics.ES31.SeparateBlendFunctions

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

### New Type OpenTK.Graphics.ES31.ShaderBinary

```
[Serializable]
public enum ShaderBinary {
	NumShaderBinaryFormats = 36345,
	ShaderBinaryFormats = 36344,
}
```

### New Type OpenTK.Graphics.ES31.ShaderBinaryFormat

```
[Serializable]
public enum ShaderBinaryFormat {
}
```

### New Type OpenTK.Graphics.ES31.ShaderParameter

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

### New Type OpenTK.Graphics.ES31.ShaderPrecision

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

### New Type OpenTK.Graphics.ES31.ShaderPrecisionSpecifiedTypes

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

### New Type OpenTK.Graphics.ES31.Shaders

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

### New Type OpenTK.Graphics.ES31.ShaderSource

```
[Serializable]
public enum ShaderSource {
	CompileStatus = 35713,
	InfoLogLength = 35716,
	ShaderCompiler = 36346,
	ShaderSourceLength = 35720,
}
```

### New Type OpenTK.Graphics.ES31.ShaderType

```
[Serializable]
public enum ShaderType {
	ComputeShader = 37305,
	FragmentShader = 35632,
	VertexShader = 35633,
}
```

### New Type OpenTK.Graphics.ES31.SizedInternalFormat

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

### New Type OpenTK.Graphics.ES31.StencilFunction

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

### New Type OpenTK.Graphics.ES31.StencilOp

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

### New Type OpenTK.Graphics.ES31.StringName

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

### New Type OpenTK.Graphics.ES31.StringNameIndexed

```
[Serializable]
public enum StringNameIndexed {
	Extensions = 7939,
}
```

### New Type OpenTK.Graphics.ES31.SyncCondition

```
[Serializable]
public enum SyncCondition {
	SyncGpuCommandsComplete = 37143,
}
```

### New Type OpenTK.Graphics.ES31.SyncParameterName

```
[Serializable]
public enum SyncParameterName {
	ObjectType = 37138,
	SyncCondition = 37139,
	SyncFlags = 37141,
	SyncStatus = 37140,
}
```

### New Type OpenTK.Graphics.ES31.TextureComponentCount

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

### New Type OpenTK.Graphics.ES31.TextureMagFilter

```
[Serializable]
public enum TextureMagFilter {
	Linear = 9729,
	Nearest = 9728,
}
```

### New Type OpenTK.Graphics.ES31.TextureMinFilter

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

### New Type OpenTK.Graphics.ES31.TextureParameterName

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

### New Type OpenTK.Graphics.ES31.TextureTarget

```
[Serializable]
public enum TextureTarget {
	MaxCubeMapTextureSize = 34076,
	Texture = 5890,
	Texture2D = 3553,
	Texture2DArray = 35866,
	Texture3D = 32879,
	TextureBaseLevel = 33084,
	TextureBindingCubeMap = 34068,
	TextureCubeMap = 34067,
	TextureCubeMapNegativeX = 34070,
	TextureCubeMapNegativeY = 34072,
	TextureCubeMapNegativeZ = 34074,
	TextureCubeMapPositiveX = 34069,
	TextureCubeMapPositiveY = 34071,
	TextureCubeMapPositiveZ = 34073,
	TextureMaxLevel = 33085,
	TextureMaxLod = 33083,
	TextureMinLod = 33082,
}
```

### New Type OpenTK.Graphics.ES31.TextureTarget2D

```
[Serializable]
public enum TextureTarget2D {
	Texture2D = 3553,
	TextureCubeMap = 34067,
}
```

### New Type OpenTK.Graphics.ES31.TextureTarget3D

```
[Serializable]
public enum TextureTarget3D {
	Texture2DArray = 35866,
	Texture3D = 32879,
}
```

### New Type OpenTK.Graphics.ES31.TextureUnit

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

### New Type OpenTK.Graphics.ES31.TextureWrapMode

```
[Serializable]
public enum TextureWrapMode {
	ClampToEdge = 33071,
	MirroredRepeat = 33648,
	Repeat = 10497,
}
```

### New Type OpenTK.Graphics.ES31.Token

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

### New Type OpenTK.Graphics.ES31.TransformFeedbackMode

```
[Serializable]
public enum TransformFeedbackMode {
	InterleavedAttribs = 35980,
	SeparateAttribs = 35981,
}
```

### New Type OpenTK.Graphics.ES31.TransformFeedbackPrimitiveType

```
[Serializable]
public enum TransformFeedbackPrimitiveType {
	Lines = 1,
	Points = 0,
	Triangles = 4,
}
```

### New Type OpenTK.Graphics.ES31.TransformFeedbackTarget

```
[Serializable]
public enum TransformFeedbackTarget {
	TransformFeedback = 36386,
}
```

### New Type OpenTK.Graphics.ES31.TransformFeedbackType

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

### New Type OpenTK.Graphics.ES31.UniformTypes

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

### New Type OpenTK.Graphics.ES31.Unknown

```
[Serializable]
public enum Unknown {
	ImgTextureFormatBgra8888 = 1,
}
```

### New Type OpenTK.Graphics.ES31.VertexArrays

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

### New Type OpenTK.Graphics.ES31.VertexAttribIntegerType

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

### New Type OpenTK.Graphics.ES31.VertexAttribParameter

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

### New Type OpenTK.Graphics.ES31.VertexAttribPointerParameter

```
[Serializable]
public enum VertexAttribPointerParameter {
	VertexAttribArrayPointer = 34373,
}
```

### New Type OpenTK.Graphics.ES31.VertexAttribPointerType

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

### New Type OpenTK.Graphics.ES31.WaitSyncFlags

```
[Serializable]
public enum WaitSyncFlags {
	None = 0,
}
```

### New Type OpenTK.Graphics.ES31.WaitSyncStatus

```
[Serializable]
public enum WaitSyncStatus {
	AlreadySignaled = 37146,
	ConditionSatisfied = 37148,
	TimeoutExpired = 37147,
	WaitFailed = 37149,
}
```
