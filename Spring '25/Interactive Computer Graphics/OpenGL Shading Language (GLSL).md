>like C++ but ==without==:
>	Pointers
>	Dynamic memory allocation
>	Recursion
>	User-defined classes
>own built-in classes:
>	vec2, vec3, vec4, mat2, mat3, mat4, etc.
>built-in linear algebra library to follow [[OpenGL Shading Language (GLSL)]] API

## Functionality
- can access the components of vectors like so:
```GLSL
vec4 v = vec4(1, 2, 3, 4);
float x = v.x;
vec2 yz = v.yz;
ve3 threeTwoOne = v.zyx;
float red = v.r; // same as v.x, just a diff name
float transparency = v.a; // a for alpha, the w coord
```
