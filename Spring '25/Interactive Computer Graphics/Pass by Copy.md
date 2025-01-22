>by default, all data passed into a scope is copied in

## Example
```C++
#include <iostream>

void foo(float a) {
	a = a * 2.f;
}

int main() {
	float x = 10.f;
	std::cout << x << std::endl;
	foo(x);
	std::cout << x << std::endl;
}
```
>**Output:** 10 and 10 