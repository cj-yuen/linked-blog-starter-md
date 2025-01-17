#function 
## [[Direct-Addressing]] Search(T, k)
```java
return T[k];
```
>**Runtime:** $O(1)$ 

## [[Chaining]] Search(T, k)
```java
search for element with key k in list T[h(k)]
```
>**Runtime:** $O(1)$

## [[Open Addressing]] Search(T, k)
```java
for i = 0 to m-1 do
	j = h(k,i)
	if T[j] == k then
		return j
	else if T[j] == null then
		return null
return null
```
>**Runtime:** $O(1)$ 