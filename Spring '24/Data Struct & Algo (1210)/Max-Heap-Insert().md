#function 
**Links:** [[Heap-Increase-Key()]]
## Max-Heap-Insert(A, key)
```java
A.heapsize = A.heapsize + 1
A[A.heapsize] = -infinity 
Heap-Increase-Key(A, A.heapsize, key)
```
>**Runtime:** $O(\lg n)$ 