#algorithm 
**Links:** [[Depth-First Search (DFS)]] 

## Kosaraju(G)
```java
// G = (V, E) : graph
// G^T = (V, E^T) = transpose of G 

DFS(G) to find finish times u.f for every vertex

compute G^T

call DFS(G^T), but in main loop of DFS, consider vertices in order of decreasing u.f

return vertices of each tree in the depth-first forest from our call DFS(G^T) as separate SCC
```
>**Runtime:** $O(V+E)$ = $O(n+m)$ 

## Lemma 
- [[Kosaraju's Lemma 1]]
- [[Kosaraju's Lemma 2]] 
- [[Kosaraju's Lemma 3]] 