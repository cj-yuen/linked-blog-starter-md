#algorithm 
## BFS(G, s)
```java
// G = (V,E) : graph as adjacency list 
// s : source vertex

for each v in V do
	discovered[v] = false

discovered[s] = true
T = 0
L[0] = {s}
i = 0
while L[i] is !empty
	let L[i+1] be new list 
	for each v in L[i] do
		for each u in Adj[v] do // neighborhood of v
			if discovered[u] = false then
				discovered[u] = true
				add (u,v) to T
				parent[u] = v
				L[i+1].append(u)
	i = i + 1

return T
```
>**Runtime:** $O(n+m)$ 
![[2019-11-13-level-order-traversal.gif]]

## Pseudocode
```java
// G = (V,E) : graph as adjacency list 
// s : source vertex

for each v in V do 
	discovered[v] = false
	parent[v] = null 

let Q be empty queue 
Q.enqueue(s)
discovered[s] = true 

while Q is !empty do
	v = Q.dequeue()
	for each u in Adj[v] do
		if discovered[u] == false then
			discovered[u] = true
			Q.enqueue(u)
			parent[u] = v
```

## BFS Properties 
1) runnable on both [[Directed]] & [[Undirected]] graphs
2) does ==not== necessarily traverse the entire graph 
	only explores nodes that are <u>reachable</u> from source node 
3) $\exists$ a path between source $s$ & some $t\in V$ $\leftrightarrow$ $t$ appears in the BFS tree 
4) for an edge $(x,y) \in G$, if $x$ & $y$ appears in the BFS tree $\rightarrow$ then for $x\in L_i$ & $y\in L_j$, $i$ and $j$ differ by $\le$ 1
	![[Pasted image 20240409150527.png]]
5) find ==shortest path== b/w 2 vertices in a <u>connected, unweighted graph</u> 
	for each node $v\in L_k$, shortest path from $s$ to $v$ is of length $k$ 
6) valid BFS trees rooted at the same source can be different 
	due to arb. processing of nodes in each layer 
7) undirected graph is bipartite $\leftrightarrow$ no 2 vertices in the same BFS layer share an edge 
	![[Pasted image 20240409151333.png]]

## Uses of BFS
1) checking connectedness of graph 
2) shortest path in [[Undirected]] graphs 
3) bipartiteness 