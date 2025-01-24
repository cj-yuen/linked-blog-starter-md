- [[Const]] objects can only call [[Const]] functions
- non-const can call whatever

## Const functions
>cannot modify any member variables of the class

### Example
```C++
int main() {
	int x = 5;
	const int& cref = x;
	x = 100;
	cref = 9;

	// cptr is a pointer to a const int
	// but the pointer itself is not const
	// and can be reassigned
	const int* cptr = &x;
	*cptr = 3;
	int y =1;
	cptr = &y; // fine, since cptr is not a const pointer
	*cptr = 2;

	int * const const_pointer_mutable_int = &x;
	*const_pointer_mutable_int = 999; // ok! the int is not a const but the
	                                  // address is const
	cptr_mutable = &y; // this is NOT allowed, cannot rebind address
}
```