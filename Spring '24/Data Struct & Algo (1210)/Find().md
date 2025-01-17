#function 

## Find(x) (Path Compression)
```java
if x != pi(x)
	pi(x) = Find(pi(x))
return pi(x)
```
>**Runtime:** $O(log^* n)$ 