>similar to [[Standard Tries]] but ensure each internal node has $\ge 2$ children by compressing chains of single-child nodes into individual edges 

given $S = \{\text{bear, bell, bid, bull, buy, sell, stock, stop}\}$
![[Pasted image 20240508123822.png]]

## Properties
1) every internal node of $T$ has $\ge 2$ children & $\le d$ children 
2) $T$ has $s$ leaves 
3) # of nodes of $T$ is $O(s)$ 