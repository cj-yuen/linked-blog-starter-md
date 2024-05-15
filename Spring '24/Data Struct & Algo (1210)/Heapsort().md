#function
**Links:** [[Max-Heapify()]]
## HeapSort(A)
```java
Build-Max-Heap(A)
for i = A.length down to 2
	exchange A[1] with A[i]
	A.heapsize = A.heapsize - 1
	Max-Heapify(A,1)
```
>**Runtime:** $O(n \lg n)$
