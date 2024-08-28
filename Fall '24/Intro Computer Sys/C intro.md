#lecture_notes  
```C
#include <stdio.h> // where printf() is 
#include <stdlib.h> // where EXIT_SUCCESS

int main(int argc, char* argv[]) {
	printf("Hello World!");
	return EXIT_SUCCESS;
}
```
>return type "int"
>indicates successful run: `EXIT_SUCCESS` or `EXIT_FAILURE`
>takes:
>	0 args 
>	CMD line args


## [[Fundamental C Types]] 


## C:printf format specifiers
>	specifies how args. to `printf` should be interpreted by using a [[format string (specifiers)]] 


## C:Function declarations
```C
type name(type1 arg1,...) {
	return [something of type type]
}
```
>runs ==top-to-bottom== 
>	the function called must be <u>declared before it is called</u> except in the case for [[Forward Declarations]] 


## Arrays
```C
type name[size]
```
- allocated `size x sizeof(type)` bytes of contiguous memory