>using <u>unary</u> * operator to access memory referred to by a [[Pointers]] 
>	used to read/write data 
```C
int *pt = ...; // assume initialized 
int a = *ptr; // read value
*ptr = a + 2; // write value
```