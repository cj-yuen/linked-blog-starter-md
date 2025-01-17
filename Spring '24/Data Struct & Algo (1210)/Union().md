#function 

## Union(x, y)
```java
r_x = FIND(x)
r_y = FIND(y)

if r_x == r_y
	return 
if rank(r_x) > rank(r_y)
	pi(r_y) = r_x
else
	pi(r_x) = r_y
	if rank(r_x) == rank(r_y)
		rank(r_y) = rank(r_y) + 1
```
