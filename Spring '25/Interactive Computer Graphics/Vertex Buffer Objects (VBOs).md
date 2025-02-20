## Visualization
![[Pasted image 20250213142603.png]]
![[Pasted image 20250213142626.png]]

## Assembly Code (floats)
```
GLuint vbo; glGenBuffers(1, &vbo); // tell OpenGL to give us a handle to a VBO it
   // creates on the GPU

std::array<float, 12> vertices; // might transfer data from a set of glm::vec3s
   // instead of hardcoding

vertices[0] = 2.0; vertices[1] = 2.0f; vertices[2] = 1.0f;
vertices[3] = 2.0f, vertices[4] = -2.0f; vertices[5] = 1.0f;
vertices[6] = -2.0f; vertices[7] = -2.0f; vertices[8] = 1.0f;
vertices[9] = -2.0f; vertices[10] = 2.0f; vertices[11] = 1.0f;

glBindBuffer(GL_ARRAY_BUFFER, vbo); // tells OpenGL that we want to put data into
   // buffer called vbo, which has been defined & bound in initialized for you

glBufferData(GL_ARRAY_BUFFER, 12*sizeof(float), vertices.data(), GL_STATIC_DRAW); 
   // gLBufferData requires a pointer to the 1st element of the float array, which
   // array::data() gives us. As exists for std::vector

glBindBuffer(GL_ARRAY_BUFFER, cbo); // do the same for our colors (pretend there's
   // another float array for colors & that we call bufferData again). Color 
   // are stored as one float for Read, Green, and Blue, and (optionally) one for 
   // Transparency, w/range [0,1]
```

## Assembly Code (vec3s)
```
GLuint vbo; glGenBuffers(1, &vbo);
std::array<glm::vec3, 4> vertices;
vertices[0] = glm::vec3(2.f, 2.f, 1.f);
vertices[1] = glm::vec3(2.f, -2.f, 1.f);
vertices[2] = glm::vec3(-2.f, -2.f, 1.f);
vertices[3] = glm::vec3(-2.f, 2.f, 1.f);

glBindBuffer(GL_ARRAY_BUFFER, vbo);
glBufferData(GL_ARRAY_BUFFER, 4*sizeof(glm::vec3), vertices.data(), GL_STATIC_DRAW);
```
- because `glm::vec3` takes up the exact same memory footprint as 3 floats, this code is equivalent the the (floats) above
- OpenGL expects all data to be floating-point numbers by default

## Example:
![[Pasted image 20250213142451.png]]

## Associating "in" variables w/[[Vertex Buffer Objects (VBOs)]]
![[Pasted image 20250213144609.png]]
![[Pasted image 20250213144616.png]]
![[Pasted image 20250213144623.png]]
![[Pasted image 20250213144718.png]]

