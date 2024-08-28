>all elements in the hash table (either element or null)
>can "fill up" s.t. no further insertions can be made ([[Load Factor]] $\alpha$ can never exceed 1)
>**Pro:** avoids points altogether & w/extra memory by no storing pointers $\rightarrow$ larger # of slots for same amount of memory (potentially less collisions & faster retrieval)

## Probe
- to perform insertion, we must successively examine/probe until we find an empty slot
- the hash function must include the probe # (starting from 0) as a 2nd input
$$h: U\times \{0,1,\dots,m-1\} \rightarrow \{ 0, 1, \dots, m-1\}$$
- for every key $k$, we require a <u>probe sequence</u> 
$$\langle h (k, 0), h(k,1), \dots, h(k,m-1)\rangle$$
	be a permutation of $\langle 0,1,\dots, m-1 \rangle$ 

We assume [[Uniform Hashing Assumption (UHA)]] 

### Types of Probing
given [[Auxiliary Hash Function]] 
1) [[Linear Probing]] 
2) [[Quadratic Probing]] 
3) [[Double Hashing]] 

## Theorem 
3) [[Hash Open-Addressing Theorem 3]] 
4) [[Hash Open-Addressing Theorem 4]] 