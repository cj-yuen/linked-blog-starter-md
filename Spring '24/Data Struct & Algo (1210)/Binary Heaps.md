>array obj. that is an almost "complete" binary tree (last level may not be "complete")
>	==height== = # of edges on the longest simple downward path from the root to a leaf
>		heap w/$n$ elements $\rightarrow$ height = $\lfloor \lg n\rfloor$ 

## Advantages ([[Priority Queues]])
- find largest element: $O(1)$
- find & extract largest element (or any other priority-queue operation on a set): $O(\log n)$ 

## Types of [[Binary Heaps]]
1) [[Max-Heaps]]
2) [[Min-Heaps]]

## Properties 
1) ==A.length== = # of elements in the array 
2) ==A.heapsize== = # of array elements that are actually part of the heap 

## Algorithms 
- [[Max-Heapify()]]
	[[Min-Heapify()]]
- [[Build-Max-Heap()]]
- [[Heapsort()]] 