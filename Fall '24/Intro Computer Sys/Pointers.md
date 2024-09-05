```C
type* name; // or type *name

```
>explicit "references" holding location to some data w/specified type

## Pointer Operators 
- [[Dereference]] & [[Reference]] 

## Pointers to Pointers to...
>can have pointers to pointers
	ie. pointer $\rightarrow$ pointer $\rightarrow$ int
```C
int x = 3;
int *ptr = &x;
int **ptr_ptr = &ptr;
```
- [[Dereference]] more than one at a time
	ie. deference's twice
```C
**ptr = 3;
```
- pointers to pointers to...
```C
int ************ptr;
```

## Difference w/[[Array]] 
>very similar
>	point can refer to 1st element in an array (can access the "index of" a pointer)
>	pointers can be reassigned while arrays cannot


### Arrays a Params (Pointer Decay)
>tricky to use arrays as params (arrays <u>do not know</u> their own ==size==)
>arrays are secretly passed as pointers to the array