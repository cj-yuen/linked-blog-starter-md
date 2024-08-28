#algorithm 

## DFS(G)
```java
// G = (V,E) : graph as adj. list

for each v in V do
	color[v] = WHITE 

time = 0

for each v in V do
	if color[v] == WHITE then
		DFS-VISIT(G, v)
```

### DFS-VISIT(G, v)
```java 
time = time + 1 
d[u] = time 
color[u] = GRAY

for each v in Adj[u] do
	if color[v] == WHITE then
		parent[v] = u
		DFS-VISIT(G, v) // go deeper into graph
color[u] = BLACK // all u's neighbors explored 
time = time + 1 
f[u] = time 
```

>**Runtime:** $O(n+m)$ 
![[tree.gif]]
- green = gray (discovered)
- orange = black (all neighbors explored)

## DFS Properties 
1) vertex $v$ is a descendant of vertex $u$ in DFS forest $\leftrightarrow$ $v$ is discovered when $u$ is grey 
2) [[Parenthesis Theorem]] 
3) [[White Path Theorem (WPT)]] 
4) [[DFS Theorem 3]]

## Edge Classifications 
![[Pasted image 20240409162023.png]]
1) [[Tree Edge]]
2) [[Back Edge]]
3) [[Forward Edge]]
4) [[Cross Edge]] 

## Uses of DFS 
1) checking connectedness 
2) topological sort (Tarjan's, Kahn's)
3) Strongly Connected Components 
4) Cycle Detection