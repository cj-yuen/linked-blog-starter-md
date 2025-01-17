#function 
## Heap-Increase-Key(A, i, key)
```java
if key < A[i]
	error "new key is smaller than current"
A[i] = key
while i > 1 && A[PARENT(i)] < A[i]
	exchange A[i] with A[PARENT(i)]
	i = PARENT(i)
```
>**Runtime:** $O(\lg n)$ 

