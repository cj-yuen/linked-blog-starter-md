#algorithm 
**LInks:** [[MakeSet()]], [[Find()]], [[Union()]] 
## Kruskal(G)
```java
// G = (V,E) : connected graph as adj. list w/positive weights

T = {} // null set 

sort edges in E in increasing weight ordre

for each v in V do
	MakeSet(v) 

for each e = (u,v) in E do
	if Find(u) != Find(v)
		T = T + {e} // union sets 
		Union(u,v)

return T 
```
>**Runtime:** $O(m\log n)$ 
![[KruskalDemo.gif]]