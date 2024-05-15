$$M = \{n_1T_1, n_2T_2, \dots, n_kT_k \} \mid n_1 + n_2 + \dots + n_k = n$$
>[[Set]] that contains multiple of the same [[Elements or Members]] 


## Permutations of $n$ objects in the [[Multiset]]
Step 1: choose $n_1$ places from $n$ places for type 1 objects ($\binom{n}{n_1}$ ways)
Step 2: choose $n_2$ places from $n$ places for type 2 objects ($\binom{n-n_1}{n_2}$ ways)
$\vdots$ 
Step $k$: choose $n_k$ places from remaining unused places for type $k$ objects ($\binom{n-n_1-\dots - n_{k-1}}{n_k}$ ways)

by [[Multiplication Rule (M.R.)]] 
$$\binom{n}{n_1} \binom{n-n_1}{n_2} \dots \binom{n-n_1-\dots - n_{k-1}}{n_k} = \frac{n_1}{n_1!n_2!\dots n_k!}$$

[[Anagrams]] = permutations of bags