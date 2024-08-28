#algorithm 
**Links:** [[Enqueue()]], [[Dequeue()]] 
## TopoSort(G)
```java
// G = (V,E) : DAG as adj. list

L : new queue // nodes of in-degree 0 (source)
OUT : new list // topo-sorted ordering 

// compute in-degree
for each v in V
	for each u in Adj[v] 
		in[u] = in[u] + 1

// initially populate L
for each v in V 
	if in[v] = 0 then
		L.enqueue(v)

while L is !empty do 
	v = L.dequeue()
	OUT.append(v)
	for each u in Adj[v] 
		in[u] = in[u] - 1
		if in[u] = 0 then 
			L.enqueue(u)

return OUT
```
>**Runtime:** $O(n+m)$ 
