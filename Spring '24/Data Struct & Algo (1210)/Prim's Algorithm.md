#algorithm 
**Links:** [[Extract-Min()]] 
## Prim(G, s) 
```java 
// G = (V, E) : connected graph as adj. list w/positive weights
// s : starting node 

let PQ be priority queue containing all vertices in G 
for each v in V do 
	v.key = infinity
	parent[v] = null

s.key = 0

while PQ is !empty do
	v = PQ.ExtractMin() 
	for each u in Adj[v] do 
		if u in PQ & w(u,v) < u.key then 
			u.key = w(u,v)
			parent[u] = v 

return parent array
```
>**Runtime:** $O(m\lg n)$ 
![[Prim-animation 1.gif]]