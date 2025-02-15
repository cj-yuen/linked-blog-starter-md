>pass vertex data from C++ program running on our CPU to the [[OpenGL]] pipeline on our [[GPU]] 
>code that does this is rather bulky
>use [[Vertex Buffer Objects (VBOs)]] to pass the data
>call several [[OpenGL]] functions from C++ code
![[Pasted image 20250211135415.png]]

## Set up Instructions
1) initialize an [[OpenGL]] connection + context
2) read + compile shader code into a ShaderProgram object
3) build VBO data for your meshes
4) associate VBOs with "in" variables in your shader
5) draw your meshes, beginning the rest of the GL pipeline