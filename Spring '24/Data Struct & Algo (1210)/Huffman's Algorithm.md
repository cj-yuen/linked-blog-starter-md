#algorithm
**Links:** [[Extract-Min()]], [[Max-Heap-Insert()]]
## Huffman(S)
```java
// S : set of chars w/char frequencies 
// Q : preiority queue containing elements in S w/frequencies as keys 

for i = 1 to n do
	allocate a new node z
	x = ExtractMin(Q)
	y = ExtractMin(Q)
	z.left = x 
	z.right = y 
	f_z = f_x + f_y
	Insert(Q,z)

return ExtractMin(Q) // root of tree
```
>**Runtime:** $O(n \lg n)$

![[Huffman_huff_demo.gif]]

## Pseudocode 
```java 
// S : set of characters w/char frequencies 

if |S| = 2 then 
	Encode 1 letter using 0 & the other using 1
else
	let y,z be the 2 lowest-frequency letters 
	
	// form new alphabet S* by deleting y & z, replacing them with new letter w w/frequence f_w
	S* = S - {y,z} + {w}
	f_w = f_y + f_z 
	
	// recursively construct a prefix code for S* w/tree T*
	T* = Huffman(S*) 
	
	// make w parent of y & z
	define a prefix code for S as follow:
		 Start with T*
		 Take leaf labeled w & add y&z as its children
```
