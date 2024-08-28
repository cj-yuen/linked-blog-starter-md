#function 
**Links:** [[Max-Heapify()]]
## Heap-Extract-Max(A)
```java
if A.heapsize < 1
	error "heap underflow"
max = A[1]
A[1] = A[A.heapsize]
A.heapsize = A.heapsize - 1
Max-Heapify(A,1)
return max
```
>**Runtime:** $O(\lg n)$ 

