#function 
## [[Direct-Addressing]] Insert(T, x)
```java
T[x.key] = x;
```
>**Runtime:** $O(1)$ 

## [[Chaining]] Insert(T, x)
```java 
insert x @head of list T[h(x.key)]
```
>**Runtime:** $O(1)$ 

## [[Open Addressing]] Insert(T, k)
```java
for i = 0 to m-1 do
	j = k(k,i)
	if T[j] == null then
		T[j] = k
		return j
return "Error: hash table overflow!"
```
>**Runtime:** $O(1)$ 