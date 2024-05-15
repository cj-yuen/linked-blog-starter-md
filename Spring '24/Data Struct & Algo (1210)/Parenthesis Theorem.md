#theorems 

>In any DFS ([[Directed]] or [[Undirected]]) graph $G = (V,E)$, for any 2 vertices $u$ & $v$, exactly 1 of the 3 must hold true
>	==(1)== intervals $[u.d, u.f]$ & $[v.d,v.f]$ are completely [[Disjoint]] $\rightarrow$ neither $u$ nor $v$ is a descendant of one another in DFS forest 
>		![[Pasted image 20240409160300.png]]
>	==(2)== interval $[u.d, u.f]$ is completely contained within interval $[v.d,v.f]$ $\rightarrow$ $u$ is a descendant of $v$ 
>		![[Pasted image 20240409160437.png]]
>	==(3)== interval $[v.d,v.f]$ is completely contained within interval $[u.d, u.f]$ $\rightarrow$ $v$ is a descendant of $u$ 
>		![[Pasted image 20240409160517.png]]

## Corollary
1) [[Nesting of Descendants' Intervals]] 
