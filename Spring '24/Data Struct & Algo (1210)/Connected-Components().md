#function 
**Links:** [[MakeSet()]], [[Find()]], [[Union()]] 
## Connected-Components(G)
```java
for each vertex v in G.V
	Make-Set(v)

for each edge (u,v) in G.E
	if Find(u) != Find(v)
		Union(u,v)
```
