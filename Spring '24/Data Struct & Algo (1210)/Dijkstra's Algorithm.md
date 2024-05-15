#algorithm  
**Links:** [[Topological Sorting]], [[Extract-Min()]],  
## Dijkstra(G,s) 
```java
// G = (V,E) : graph as adj. list
// s : source vertex 

for each v in V do 
	dist[v] = infinity 
	parent[v] = null

dist[s] = 0

S = {} // null set
Q // min-priority queue on all vertices, keyed by dist values

while Q is !empty do
	u = Extract-Min(Q)
	S = S + {u} // union of S & u
	for each v in Adj[u] do 
		// edge relaxation step
		if v in Q & dist[v] > dist[u] + w(u,v) then
			dist[v] = dist[u] + w(u,v) // decrease-key operation
			parent[v] = u
```
>**Runtime:** $O(n+m)$ 
![[dijkstra.gif]]