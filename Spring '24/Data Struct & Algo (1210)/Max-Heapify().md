#function 
**Links:** [[Max-Heapify()]]
## Max-Heapify(A, i)
```java 
l = Left(i)
r = Right(i)
if l <= A.heapsize && A[l] > A[i]
	largest = l
else 
	largest = i

if r <= A.heapsize && A[r] > A[largest] 
	largest = r
if largest != i
	exchange A[i] with A[largest]
	Max-Heapify(A,largest)
```
>**Runtime:** $O(\lg n)$
![[Pasted image 20240405190048.png]]
	![[Pasted image 20240405190104.png]]
		![[Pasted image 20240405190122.png]]

