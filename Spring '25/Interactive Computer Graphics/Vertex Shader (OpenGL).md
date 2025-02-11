>takes in [[Vertex Data (OpenGL)]] & <u>applies transformations to it</u> 
>[[GPU]]'s have many execution threats with which to run shaders	
>each [[Vertex Shader (OpenGL)]] instance is given one vertex
>all instances apply same transformation(s) to their vertex
![[Pasted image 20250211135538.png]]

## [[Shaders]]

## Sample Vertex Shader Code
```GLSL
#version 150 // Specify which version of GLSL the compiler should use (1.5 correlates to OpenGL 3.2)

uniform mat4 u_ViewProj; // the view & projection matrices concatenated into one
   // it's uniform since every vertex shader instance uses the same camera

in vec4 vs_Pos; // pos of the vertex
in vec4 vs_Col; // color of the vertex

out vec4 fs_Coll; // vertex color to pass down the pipelines to fragment shader

void main() {
	fs_Col = vs_Col; // pass the vertex color to the fragment shader
	
	gl_Position = u_ViewProj * vs_Pos; // gl_Position is a built-in keyword that
	   // stores the final position of the vertex being processed by this shader
}
```
