
![[Pasted image 20250211135305.png]]
1) [[Vertex Data (OpenGL)]]
2) [[Vertex Shader (OpenGL)]] 
	first programmable step (executed on [[GPU]])
3) [[Primitive Assembly (OpenGL)]] 
4) [[Rasterization (OpenGL)]] 
5) [[Fragment Shader (OpenGL)]] 
6) [[Frame Buffer (OpenGL)]] 

## Initialize an [[OpenGL]] Context
- establish a connection between the CPU & GPU
- in code we work with, this is the call to `initializeGL()` in MyGL (becomes your "OpenGL context)
	without this, cannot invoke OpenGL functions

## Compiling shader code
- C++ program passes .glsl ASCII text to GPU
	`glShaderSource()`
- GPU then compiles those .glsl files into vertex & fragment shaders
	`glCompilerShader()`
- GPU is then told to assemble those shaders into an overall shader program
	`glAttachShader()`, `glLinkProgram()`
- look at `ShaderProgram::create()` for all the code in action

## Assemble [[Vertex Buffer Objects (VBOs)]] data
- assemble all per-vertex data into float array(s) & buffer it to the GPU
	the less often you pass data to the GPU, the better
	same goes for quantity of data passed
- minimum data needed to view geometry: ==vertex positions== & ==triangle indices== 

## Tracking objects on the GPU
- can't directly access GPU memory
- track "objects" we create on the GPU through handles
	typically ints, GLuints
 - initialize a GPU-side object w/code similar to this:
	 `GLunit vbo; glGenBuffers(1, &vbo);`
- the code above tells the GPU to instantiate a buffer object & store a unique ID for it in the GLuint name `vbo`
![[Pasted image 20250213142431.png]]

## Why use Index Buffers?
![[Pasted image 20250213142536.png]]
![[Pasted image 20250213142544.png]]
