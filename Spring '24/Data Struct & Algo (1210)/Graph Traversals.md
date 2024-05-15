[[Graph]] $G = (V,E)$ w/$n$ vertices & $m$ [[edge]] 

## Types of [[Graph]]
- [[Directed]]
	$m\le n(n-1)$ 
		$m = O(n^2)$ 
		$m = O(\log n)$ 
- [[Undirected]]
	$m \le \frac{n (n-1)}{2}$
- [[Connected]]
	& [[Undirected]]: $m \ge n-1$ 
- [[Sparse]]
- [[Dense]]

## Graph Representations
1) [[Adjacency Matrix]]
2) [[Adjacency List]] 

## Comparison
| **Property**                                         | [[Adjacency Matrix]] | [[Adjacency List]]             |
| ---------------------------------------------------- | -------------------- | ------------------------------ |
| check edge existence                                 | constant time        | iterates up to $\text{deg}(i)$ |
| Space                                                | $\Theta(n^2)$        | $\Theta(m+n)$                  |
| # of operations to enumerate neighbors of vertex $v$ | $\Theta(n)$          | $\text{deg}(v)$ time           |
>if [[Sparse]] $\rightarrow$ [[Adjacency List]] ($m \ll n^2$)
>if [[Dense]] $\rightarrow$ [[Adjacency Matrix]] ($m \approx n^2$)


## Connectivity
- given graph $G = (V,E)$, we ask the question
>"Is there a path from $s$ to $t$ in $G$?"
>	concerning $s$-$t$ connectivity 
>	aka traversal problem: "From $s$, which nodes are reachable?"


## Solutions to Connectivity/Traversals
1) [[Breadth-First Search (BFS)]] 
2) [[Depth-First Search (DFS)]] 

## Differences between [[Breadth-First Search (BFS)]] & [[Depth-First Search (DFS)]] 
![[Pasted image 20240409150200.jpg]]

