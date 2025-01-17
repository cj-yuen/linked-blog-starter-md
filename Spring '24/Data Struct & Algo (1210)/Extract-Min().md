#function 
**Links:** [[Min-Heapify()]]
## Heap-Extract-Min(A)
```java
if A.heapsize < 1
	error "heap underflow"
min = A[1]
A[1] = A[A.heapsize]
A.heapsize = A.heapsize - 1
Min-Heapify(A,1)
return max
```
>**Runtime:** $O(\lg n)$ 

