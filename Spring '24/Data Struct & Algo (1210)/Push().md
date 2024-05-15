#function
## Push(obj.)
```java
// s: stack size 
// a: array size
// c: inital size of array 
// A[0,...,a-1]

A[s] <- obj
s++ 
if s==a then
	a <- 2*a
	copy all elems to new array
```
>**Amortized Runtime:** $O(1)$
>**Example**
>	![[Pasted image 20240405154422.png]]

