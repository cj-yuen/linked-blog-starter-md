#algorithm 

## Reverse-Delete(G)
```java 
// G = (E, V) : connected graph as adj. list w/positive weights 

T = E 

sort edges in E in decreasing order of weight 

for each e = (u,v) in E do
	if T - {e} is connected 
		T = T - {e}

return T
```
>**Runtime:** $O(m^2)$ 
