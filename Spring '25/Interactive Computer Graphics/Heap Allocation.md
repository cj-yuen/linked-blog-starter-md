`#include <memory>`

## C-Style 
```C++
float* x = (float*)malloc(sizeof(float));
*x = 5;
```

## C++95 Style
```C++
float* y = new float(5);

delete x; // deallocate the heap mem pionted to by x
```

## C++20 Style (preferred)
```C++
std::uniqud_ptr<float> z = std::make_unique<float>(5);
```


## Other Operations
### std::move
1) temporarily un-link the address the pointer owns from the pointer
2) set the pointer to null
3) return the un-linked value so it can be stored in a diff unique ptr

```C++
std::unique_ptr<int> x = std::make_unique<int>(5);
std::cout << "x's value is " << x.get() << std::endl;

uPtrExample(std::move)
sd::cout << "x's value is " << x.get() << std::endl;
// std::unique_ptr<int> y = x;
```

