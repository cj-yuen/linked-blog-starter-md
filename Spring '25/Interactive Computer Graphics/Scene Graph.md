>set of nodes that hold transformation matrix data & pointers to other nodes & geometry
>	traverse a directed tree of transformations to render shapes
>![[Pasted image 20250124150503.png]]

## Traversing a [[Scene Graph]]
```C++
Traverse (Node n, Matrix T) {
	T = T * n.matrix()
	for each (Node child in n.children) {
		Traverse(child, T)
	}
	if (n has geometry) {
		draw(n.geometry, T)
	}
}
```
>recursively traverse each node's children until reaching a leaf node