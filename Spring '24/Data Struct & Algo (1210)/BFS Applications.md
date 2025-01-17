## Definitions & Properties 
- [[Bipartite]] 
- **Proposition 1**
	if a graph $G$ is [[Bipartite]] $\leftrightarrow$ then it has no odd length cycles 
- **Proposition 2**
	let graph $G$ be a [[Connected]] graph & let $L_0, L_1, \dots$ be the layers produced by [[Breadth-First Search (BFS)]] starting @node $s$, exactly 1 of the 2 things must hold:
		==(1)== $\not\exists$ edge of $G$ joining 2 nodes of the same layer $\rightarrow$ $G$ is a [[Bipartite]] graph (2-colorable)
		==(2)== $\exists$ edge of $G$ joining 2 nodes of the same layers $\rightarrow$ $G$ contains an <u>odd length cycle</u> 
- [[BFS Theorem 1]] 