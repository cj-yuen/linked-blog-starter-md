>resolves [[Collision]] by placing all element that hash into the same slot into the same linked list
![[Pasted image 20240502202232.png]]

## Analysis 
<u>Worst-Case Behavior:</u> all $n$ keys hash to same slot (list w/length $n$)
	Search() worst-case time $\Theta(n)$ 

<u>Average-Case Behavior:</u> depends on hash function $h$ distribution of the set of keys among the $m$ slots (seeking even distribution of universe $U$ keys )

[[Simple Uniform Hashing Assumption (SUHA)]] 

## Theorems
1) [[Hash Chaining Theorem 1]] 
2) [[Hash Chaining Theorem 2]] 