#function 
## [[Direct-Addressing]] Delete(T, k)
```java
T[k] = null;
```
>**Runtime:** $O(1)$ 

## [[Chaining]] Delete(T, x)
```java
delete x from list T[h(x.key)]
```
>**Runtime:** $O(1)$ 

## [[Open Addressing]] Delete(T, x)
>difficult as we <u>cannot</u> mark that slot as empty by storing NIL (if so we might be unable to retrieve any key $k$ during whose insertion we had probed slot $i$ & found it occupied)
>	could mark the slot a special value DELETED instead of NIL & then modify Insert() to treat slot as if it were empty