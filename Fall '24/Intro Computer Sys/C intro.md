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
- normal usage = compile-time constant for size
	`int scores[5];
- initially <u>array values are "garbage"</u> 
	![[Pasted image 20240827230235.png]]

### Array Size
* ==not stored anywhere== 
	the array does not know its own size!!!
- will have to store the length in another variable/hard-code it 

### Array Initialization
```C
type name[size] = {val0,...,valN};
```
* {} initialization can only be used at <u>time of definition</u>
* if no `size` supplied, infers from length of array initializer
* array name = identifier for "collection of data"
	`name[index]` specifies an elem. of the array & can be used as an assignment target/value in an expression

>Array name (by itself) produces the <u>address of the start of the array</u> 
>	array name ==cannot be assigned to / changed== 
```C
int primes[6] = {2, 3, 5, 6, 11, 13};
primes[3] = 7;
primes[100] = 0; // memory smash
```
### Arrays as Params.
- arrays do not know their own size 
	![[Pasted image 20240827230919.png]]
- pass another param. `size` 
	![[Pasted image 20240827230946.png]]


## C CMD line args
```C
#include <stdio.h>
#include <stdib.h>

int main(int argc, char* argc[]) {
	for (int i = 0; i < argc; i++) {
		printf("%s\n", argv[i]);
	}
	return EXIT_SUCESS;
}
```
>`argc` = # of args. given to the program
>	name of the program counts as an arg.
>`argv` = array of char*'s (strings) that are args.
>	name of the program is the first arg.


## Formatted I/O
- many programs need to covert bit values & human readable code
- often done by following functions/variants
	[[printf]] 
	[[scanf]] 

## String w/o Objects
- strings are <u>central</u> (very important for I/O)
- in C there are no Objects but we need strings
- if a string is just a seq. of chars. -> use array of chars. as string

```C
char str_arr[] = "Hello World!";
char *str_ptr = "Hello World!";
```

## Null Termination
- mark end of a string w/[[Null Terminator Character]] 

## [[Pointers]] 
