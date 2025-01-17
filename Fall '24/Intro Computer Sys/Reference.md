>use & to get the [[Reference]] of a variable
```C
int a = 240;
int *ptr = &a;
*ptr = 2; // 'a' now holds 2
```

## Null
>reference <u>guaranteed to be invalid</u> (attempt to [[Dereference]] NULL $\rightarrow$ segmentation fault)
>	used as indicator of an uninitialized (unused) pointer
>		better to cause a ==segfault== than to allow corruption of memory

```C
int main(int argc, char* argv[]) {
	int* p = NULL; 
	*p = 1; // causes segfault
	return EXIT_SUCCESS
}
```