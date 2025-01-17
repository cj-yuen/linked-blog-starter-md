### main.cpp
```C++
#include <iostream> 
#include "vec3.h"

// C++ standard library
// Indicated by the use of std:: prefix
// Must #include the appropriate standard library header
// (use <> for including STL components)
// e.g. #include <iostream>

// The :: symbols indicates that you want the compiler to 
// look for a token in a particular namespace

int main() {
//	int cout = 1; 
//	std::cout << "Hello World " << std::endl;

	vec3 a(1, 2, 3); // vec2 a = vec3(1,2,3);
	float x = a[0];

	std::cout << "x is " << x << std::endl;

	// Const variables' values cannot be changed
	// once set, AND they must be assigned a value
	// on the same line they're declared.
	const int b = 5
	// b = 0; cannot work

	return 0;
}
```


### vec3.h
```C++
#ifndef VEC3_H
#define VEC3_H
// ^ This is an include guard
// Prevents the compiler from compiling
// the same tokens mor ethan once, causing
// it to think you've defined something more than once

#endif // VEC3_H
```

or 

```C++
#pragma once

#include <array>

// This class will represent a vector of length 3
// that contains floats
class vec3 {
private: 
	float x, y, z;

	std::array<float, 3> example; // C++-style array
//	float arr[3]; // C-style array

public:
	vec3();
	vec3(float);
	vec3(float, float, float);

	// a const FUNCTION cannot modify any members 
	// of the invoking class
	float operator[](unsigned int) const;
};
```
>Visibility of certain parts of classes

### vec3.cpp
```C++
#include "vec3.h"
#include std::out_of_range // something like that

vec3::vec3(float f)
	: vec3(f,f,f)
{}

vec3::vec3(float x, float y, float z)
	: x(s), y(y), z(z), example{x,y,z}
{}

vec3::vec3()
// The : between () and { indicates 
// that you are defining your constructor's
// initializer list (used to set initial values)
	: vec3(0)
{
// NEVER ASSIGNMENT MEMBERS THIS WAY
// x = 0;
// y = 0;
// z = 0;
}

float vec3::operator[](unsigned int i) const {
	switch(i) {
	case 0:
		return x;
	case 1:
		return y;
	case 2:
		return z;
	default:
		throw std::out_of_range("index is out of range!");
	}
}
```
>Initializing variables


---
## Pointers & References
```C++
vec3* ptr = &a; 
// * next to the variable type indicates it's a pointer to something of that type
// &a is shorthand for "get the memory address of a"

// A pointer's literal value is a memory address 
// As such, regardless of what a pointer points to, a pointer's
// memory footprint is fixed (32 bits or 64 bits depending on your OS)

std::cout << "a.x before manipulation: " << a[0] << std::endl;
(*ptr).x = 100;
std::cout << "a.x after manipulation: " << a[0] << std::endl;

// A reference is like an alias of something else in your
// program. Anything you do to a reference you actually do to 
// the object it's bound to.
vec3& ref = a;
std::cout << "a.x before manipulation: " << a[0] << std::endl;
ref.x = 99999;
std::cout << "a.x after manipulation: " << a[0] << std::endl;
```

```C++
// L-value: Must exist on the left-hand side of an = (can be assigned a value)
// R-value: Must exist on the right-hand side of an = (cannot be assigned a new value)
```