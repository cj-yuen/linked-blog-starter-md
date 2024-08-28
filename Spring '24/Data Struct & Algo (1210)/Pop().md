#function 
## Pop()
```java
// s: stack size 
// a: array size
// c: inital size of array 
// A[0,...,a-1]

item = A[s]
s = s - 1 
if s < a/4 then
	a = a/2
```
>**Amortized Runtime:** $O(1)$
